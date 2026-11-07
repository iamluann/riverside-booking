# Learning log

## Session 1 · 6–7 Nov 2026 · Lab and Linux workstation
- **Did:** Built a nested-virtualisation lab VM in Hyper-V, installed WSL2 Ubuntu 26.04, Docker Engine, VS Code and Git with SSH to GitHub.
- **Broke:** `docker` gave permission denied after adding myself to the docker group.
- **Root cause:** group membership only applies to new login sessions; WSL kept the old one running.
- **Fix:** `wsl --shutdown`, reopened Ubuntu, confirmed with `groups`.
- **Learned:** checkpoints before risky changes; qualify commands when two modules clash (Hyper-V vs PowerCLI `Stop-VM`).

## Session 2 · 7 Nov 2026 · Files, folders and permissions
- **Did:** Walked the file tree, created the project layout, practised chmod, explored /var/log.
- **Learned:** `chmod +x` adds execute but doesn't set exact permissions; `>` replaces contents but keeps existing permissions; 600 is for secrets.