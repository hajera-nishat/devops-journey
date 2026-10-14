# DevOps Journey Log

Daily log of what I built, what broke, and what I learned.

Format: `Date | Hours | Built | Broke | Learned`

---

## 2026-10-14

**Hours:** ~3

**Built:**
- Verified WSL2 + Ubuntu on Windows
- Git 2.34.1, Docker 29.7.2, Go 1.27.1 all working inside Ubuntu
- GitHub 2FA enabled (authenticator app)
- Docker Desktop WSL integration enabled

**Broke:**
- `docker --version` returned "command not found" inside Ubuntu
  even though Docker Desktop was installed on Windows
- Fixed by enabling WSL integration in Docker Desktop → Settings → Resources → WSL Integration

**Learned:**
- Docker Desktop on Windows does not automatically expose the `docker`
  CLI inside WSL distros; WSL integration must be explicitly enabled per distro
- Go installs cleanly from the official tarball into `/usr/local/go`,
  and requires a PATH update in `~/.profile`

---
