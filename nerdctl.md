# Install nerdctl with build on WSL2

## Installation and prerequisites

```bash
# Install containerd + nerdctl

sudo apt update
sudo apt install -y containerd runc

# Download nerdctl (example: latest release)

VERSION=$(curl -s https://api.github.com/repos/containerd/nerdctl/releases/latest | grep tag_name | cut -d '"' -f4)
curl -L https://github.com/containerd/nerdctl/releases/download/${VERSION}/nerdctl-${VERSION#v}-linux-amd64.tar.gz | sudo tar -C /usr/local/bin -xz

# Install CNI plugins (for networking)

curl -L https://github.com/containernetworking/plugins/releases/latest/download/cni-plugins-linux-amd64.tgz | sudo tar -C /opt/cni/bin -xz

# Install BuildKit

BKVERSION=$(curl -s https://api.github.com/repos/moby/buildkit/releases/latest | grep tag_name | cut -d '"' -f4)
curl -L https://github.com/moby/buildkit/releases/download/${BKVERSION}/buildkit-${BKVERSION}.linux-amd64.tar.gz | sudo tar -C /usr/local -xz

# Create a buildkit.service file

sudo tee /etc/systemd/system/buildkit.service <<'EOF'
[Unit]
Description=BuildKit daemon
Documentation=https://github.com/moby/buildkit
After=network.target containerd.service
Requires=containerd.service

[Service]
ExecStart=/usr/local/bin/buildkitd --group containerd
Restart=always

[Install]
WantedBy=multi-user.target
EOF

# Add groups

sudo groupadd --system containerd
sudo buildkitd --group containerd

```

## Endable services

```bash

# Start containerd
sudo systemctl enable --now containerd

# Start BuildKit daemon
sudo systemctl enable --now buildkit

```

## Run a container

```bash
sudo nerdctl run -d --name web -p 8080:80 nginx:alpine
```

## Build a container

```bash
sudo nerdctl build -t myapp:latest .
```

## Push to registry

```bash
sudo nerdctl push myregistry.local/myapp:latest
```
