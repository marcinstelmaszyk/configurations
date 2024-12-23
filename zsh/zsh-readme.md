## Change the shell to Zsh

#### Install [Z shell](https://en.wikipedia.org/wiki/Z_shell)
```bash
sudo apt-get update && sudo apt-get install zsh
```
#### Install [Oh My Zsh](https://ohmyz.sh/)
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

#### Install [powerlevel10k](https://github.com/romkatv/powerlevel10k) theme
1. Clone the repository
    ```zsh
    git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
    ```
2. Update the value of `ZSH_THEME` in `~/.zshrc`:
    ```zsh
    sed -i "s/ZSH_THEME=\".*\"/ZSH_THEME=\"powerlevel10k\/powerlevel10k\"/" ~/.zshrc
    ```
#### Install plugin [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting/)
1. Clone the repository
    ```zsh
    git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
    ```
2. Activate the plugin in `~/.zshrc`:
    ```zsh
    sed -i 's/^plugins=(\(.*\))/plugins=(\1 zsh-syntax-highlighting)/' ~/.zshrc
    ```

#### Install plugin [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)
1. Clone this repository into `$ZSH_CUSTOM/plugins`
   ```zsh
   git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
   ```
2. Activate the plugin in `~/.zshrc`:
    ```zsh
    sed -i 's/^plugins=(\(.*\))/plugins=(\1 zsh-autosuggestions)/' ~/.zshrc
    ```

#### Add user aliases
```zsh
echo "alias cll='clear; ll'" >> ${ZSH_CUSTOM}/aliases.zsh
```
