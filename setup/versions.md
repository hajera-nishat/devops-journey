# Verified tool versions

Environment: Windows 11 + WSL2 (Ubuntu 22.04 "jammy"), architecture x86_64

Verified on: 2026-10-14

| Tool | Command | Output |
|---|---|---|
| Git | `git --version` | `git version 2.34.1` |
| Docker | `docker --version` | `Docker version 29.7.2, build a7dcaa6` |
| Go | `go version` | `go version go1.27.1 linux/amd64` |

## Install notes

- **WSL2:** already installed; Ubuntu was set as the default distribution (`wsl --status` reported Default Version: 2)
- **Docker:** Docker Desktop for Windows was already installed. The CLI was not available inside Ubuntu until WSL integration was enabled in Docker Desktop → Settings → Resources → WSL Integration → Apply & Restart
- **Go:** installed from the official tarball, not from apt:
  - `wget https://go.dev/dl/go1.27.1.linux-amd64.tar.gz`
  - `sudo tar -C /usr/local -xzf go1.27.1.linux-amd64.tar.gz`
  - `echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.profile`
  - `source ~/.profile`
