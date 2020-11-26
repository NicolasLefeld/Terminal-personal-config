# Install [Zsh](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)

1. There are two main ways to install Zsh
* with the package manager of your choice, e.g. sudo apt install zsh (see below for more examples)
* from source, following instructions from the Zsh FAQ
2. Verify installation by running zsh --version. Expected result: zsh 5.4.2 or more recent.
3. Make it your default shell: chsh -s $(which zsh)
* Note that this will not work if Zsh is not in your authorized shells list (/etc/shells) or if you don't have permission to use chsh. If that's the case you'll need to use a different procedure.
4. Log out and log back in again to use your new default shell.
5. Test that it worked with echo $SHELL. Expected result: /bin/zsh or similar.
6. Test with $SHELL --version. Expected result: 'zsh 5.4.2' or similar

# Install [Spaceship](https://github.com/denysdovhan/spaceship-prompt) theme

1. Clone this repo:

```
git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
```

2. Symlink spaceship.zsh-theme to your oh-my-zsh custom themes directory:

```
ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme" 
```

Set ZSH_THEME="spaceship" in your .zshrc.

