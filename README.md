# local-dev
## Local Environment Tools
    - `.zshrc.sh`: My zsh for local development
    - `nvim/`: Neovim configuration

## Neovim Setup
### Setup on a new machine (Ubuntu / WSL)

**Prerequisites**

```bash
sudo apt update && sudo apt install -y git curl unzip build-essential ripgrep fd-find fzf

# Neovim (latest stable)
curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim-linux-x86_64.tar.gz
sudo rm -rf /opt/nvim && sudo tar -C /opt -xzf nvim-linux-x86_64.tar.gz
echo 'export PATH="$PATH:/opt/nvim-linux-x86_64/bin"' >> ~/.bashrc && source ~/.bashrc

# Go (for lang.go)
curl -LO https://go.dev/dl/go1.23.4.linux-amd64.tar.gz
sudo rm -rf /usr/local/go && sudo tar -C /usr/local -xzf go1.23.4.linux-amd64.tar.gz
echo 'export PATH="$PATH:/usr/local/go/bin:$HOME/go/bin"' >> ~/.bashrc && source ~/.bashrc
```

```
```
**Clone config**

```bash
mv ~/.config/nvim{,.bak} 2>/dev/null
git clone https://github.com/bpalko/local-dev.git ~/.config/nvim
nvim
```

First launch installs all plugins and LSPs automatically. Install a Nerd Font in your terminal for icons.
