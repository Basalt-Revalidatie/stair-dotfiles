## What is this?

These are the dotfiles for the Stair Challenge - Raspberry Pi. It is recommended
that you install the additional packages only if you are using a Raspberry Pi 4 with
enough RAM, to avoid slowing down your Pi.

## How to install configuration?

```bash
git clone https://github.com/klaasnicolaas/stair-dotfiles.git
cd ~/stair-dotfiles && bash install.sh
```
After the installation, first reboot the Raspberry Pi.

## Installed packages

The following platforms are installed and set up by default with the bash script:

- GitHub CLI
- Oh My Zsh (with powerlevel10k)
- Pyenv
- Nvm
- Docker
- Docker Compose

## Manual installations

After installation, there are still a few things I always do manually.

This is the case for:

- Python
- GitHub
- Node.JS/NPM
- Poetry

### Install a python version

```bash
pyenv install --list | grep " 3\.[91011]"
pyenv install 3.11
pyenv global 3.11
```

### Setup Github account

```bash
git config --global user.name "Basalt Revalidatie"
git config --global user.email "hello@example.com"
```

### Setup Node.JS/NPM

```bash
nvm install 18
nvm use 18
nvm alias default 18
```

### Install Poetry

_Note: This can only after installing python._

```bash
bash components/poetry.sh
```