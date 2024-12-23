#### Install zsh
```bash
sudo apt-get update && sudo apt-get install zsh
```

#### Edit ~/.zshrc

```zsh
# File .zshrc

source ~/.zsh/powerlevel10k/powerlevel10k.zsh-theme

# Aliases
alias ll='ls -l'
alias cll='clear; ll'

# Autosuggestions
source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh

```
To customize prompt, run `p10k configure` or edit ~/.p10k.zsh.
[[ ! -f ~/.p10k.zsh ]] || source ~/.p10k.zsh
