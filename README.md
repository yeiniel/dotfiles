# Dotfiles

My personal dotfiles managed with [yadm](https://yadm.io/).

## Quick Setup

### Method 1: Direct execution (recommended)
```bash
wget -qO- https://raw.githubusercontent.com/yeiniel/dotfiles/main/.config/yadm/bootstrap | bash
```

### Method 2: Using yadm clone
```bash
sudo pacman -S yadm
yadm clone https://github.com/yeiniel/dotfiles
# Bootstrap script runs automatically after clone
```

## What's Included

- **Git configuration** (`.gitconfig`)
- **GPG configuration** (`.gnupg/gpg.conf`, `.gnupg/gpg-agent.conf`)
- **SSH configuration** (`.ssh/config`)
- **GPG signing key** (`.gnupg/my-signing-key.asc`)
- **SSH control for GPG agent** (`.gnupg/sshcontrol`)

## What the Setup Does

1. Updates system packages
2. Installs essential packages (git, gnupg, openssh, yadm)
3. Clones dotfiles repository
4. Restarts GPG agent with SSH support
5. Tests SSH connection to GitHub

## Requirements

- Fresh Arch Linux installation (blank archinstall profile)
- Internet connection
- Your GPG key should be added to GitHub for SSH authentication