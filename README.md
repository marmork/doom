# 1. Installation of Doom Emacs

## 1.1 Preparations

```bash
sudo apt update
sudo apt install git ripgrep fd-find sqlite3
```

## 1.2 Installation

During installation, two folders are created:
1. emacs/
2. doom/
We only work in the doom folder, as this is where we configure the settings. The cache is located under ~/.emacs.d.

* Clone repository: `git clone --depth 1 https://github.com/doomemacs/doomemacs ~/.config/emacs`  
* Install: `~/.config/emacs/bin/doom install`

After successful installation, the following text appears:  
```bash
But before you doom yourself, here are some things you should know:

1. Don't forget to run 'doom sync' and restart Emacs after modifying init.el or
   packages.el in ~/.config/doom. This is never necessary for config.el.

2. If something goes wrong, run `doom doctor` to diagnose common issues with
   your environment, setup, and config.

3. Use 'doom upgrade' to update Doom. Doing it any other way will require
   additional steps (see 'doom help upgrade').

4. Access Doom's documentation from within Emacs via 'SPC h d h' or 'C-h d h'
   (or 'M-x doom/help').

Have fun!
```

## 1.3. Add Doom Emacs to PATH

```bash
nano ~/.config/fish/config.fish
# Add Doom Emacs to PATH
set -gx PATH $HOME/.config/emacs/bin $PATH
source ~/.config/fish/config.fish
```

If `which doom` shows `/home/<username>/.config/emacs/bin/doom` and the output of `doom --version` is not empty, then the installation was successful.

# 2. Set-up

## 2.1 How do I keep Doom Emacs up to date?

* For regular maintenance, simply run: `doom sync`
* To upgrade, run the following commands:  
  ```bash
  cd ~/.config/emacs
  git pull
  doom upgrade
  ```
