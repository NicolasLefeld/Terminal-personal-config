# Prerequisites
In order to install and setup ZSH and Oh-My-Zsh on Ubuntu 20.04, there are a few tools we will need. These include wget, curl and git. They can be installed by running the command below

> apt install wget curl git -y

# Instalation
1. Install zsh

> apt install zsh

2. Change the default terminal to zsh

> chsh -s $(which zsh)

3. Install Oh-my-Zsh 

> sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

# Setup
1. Clone this 2 repos, they contain the plugins

```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:=~/.oh-my-zsh/custom}/plugins/zsh-completions

git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

```

2. Then run this command

> nano ~/.zshrc

3. Locate the ZSH_THEME and change it to

> ZSH_THEME="powerlevel10k/powerlevel10k"

4. Locate the plugins and change it to

> plugins=(git zsh-autosuggestions zsh-completions)

5. Under plugins add

> autoload -U compinit && compinit

# Powerlevel10k Setup

1. Run the command bellow and configure the powerlevel10k theme to your like!

> p10k configure