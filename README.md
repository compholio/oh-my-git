# oh-my-git!


![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/oppa-lana-style/images/samples/01-ordinary-prompt.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/oppa-lana-style/images/samples/02-bang.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/oppa-lana-style/images/samples/03-useful-information.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/oppa-lana-style/images/samples/04-untracked-files.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/oppa-lana-style/images/samples/06-rm-commit.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/oppa-lana-style/images/samples/06-tris-colors.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/oppa-lana-style/images/samples/07-tracking-branches.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/oppa-lana-style/images/samples/08-push-rebase-and-remote-branch-names.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/oppa-lana-style/images/samples/09-you-can-push.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/oppa-lana-style/images/samples/10-you-are-behind-fast-forward.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/oppa-lana-style/images/samples/11-diverged.jpg)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/oppa-lana-style/images/samples/12-detached.jpg	Oppa-lana-style)
![alt tag](https://raw.githubusercontent.com/arialdomartini/oh-my-git-gh-pages/oppa-lana-style/images/samples/13-stash-and-tag.jpg)


![alt tag](https://raw.github.com/arialdomartini/oh-my-git-gh-pages/gh-pages/images/shut-up.gif)


# Bash

## Installation

One liner for Mac:

    cd ~ && git clone https://github.com/arialdomartini/oh-my-git.git && echo source $HOME/oh-my-git/prompt.sh >> .profile


One liner for Ubuntu:

    cd ~ && git clone https://github.com/arialdomartini/oh-my-git.git && echo source $HOME/oh-my-git/prompt.sh >> .bashrc

Then, set your Terminal font to Monospace (or edit oh-my-git and change the symbols used)

## Manual installation

Fork the repo and git clone it in your home directory.

Then add

    source $HOME/oh-my-git/prompt.sh

to the bash startup file (`~/.profile` on Mac, `~/.bashrc` on Linux)

If you prefer to keep oh-my-git repository in a different directory, just modify the startup file accordingly to the chosen position

    source /wherever-you-want/oh-my-git/prompt.sh

# zsh

## Installation

With antigen installed, just add

    antigen-bundle arialdomartini/oh-my-git
    antigen theme arialdomartini/oh-my-git-themes arialdo-granzestyle

to your `.zshrc` file.

[`oh-my-git-themes`](https://github.com/arialdomartini/oh-my-git-themes) includes two themes: `arialdo-granzestyle` which is inspired to the great [Granze theme](https://github.com/Granze/G-zsh-theme-2), and `arialdo-pathinline`.

## How to install antigen

[antigen](https://github.com/zsh-users/antigen) is a plugin manager for `zsh`.
Installing antigen is straightforward:

    cd ~ && git clone https://github.com/zsh-users/antigen.git .antigen 

Then, edit your `.zshrc` file including

    source "$HOME/.antigen/antigen.zsh"

    antigen-bundle arialdomartini/oh-my-git
    antigen theme arialdomartini/oh-my-git-themes arialdo-granzestyle

    antigen-apply

I also strongly suggest to include

    antigen-use oh-my-zsh
    antigen-bundle git
    antigen-bundle zsh-users/zsh-syntax-highlighting
    antigen-bundle zsh-users/zsh-history-substring-search

which are optional, but very cool.

Then, restart zsh. 
antigen will download and install all that's needed.

# Disabling oh-my-git
oh-my-git can be disabled on a per-repository basis. Just add a

    [oh-my-git]
    enabled = false

in the `.git/config` file of a repo to revert to the original prompt for that particular repo. This could be handy when working with very huge repository, when the git commands invoked by oh-my-git can slow down the prompt.


# Known bugs and limitations

* git v1.8.4 or newer is required
* It works weird on brand new repositories, before the first commit
* It has been tested on Mac and Ubuntu only. I never managed to make it work on Cygwin
* You need an unicode font (like Menlo or Monaco on Mac OS X, or Monospace on Ubuntu; on Windows, with Cygwin, a good choice is [Meslo](https://github.com/andreberg/Meslo-Font) by [André Berg](https://github.com/andreberg))
* With the default Ubuntu terminal font, some symbols are not properly displayed. Use Monospace, or edit the `prompt.sh` file and choose other symbols
