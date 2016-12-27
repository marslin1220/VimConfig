# Synchronizing plugins with git submodules and pathogen


## Installation

```sh
git clone git@github.com:marslin1220/VimConfig.git ~/.vim
```
## Create symlinks

```sh
ln -s ~/.vim/vimrc ~/.vimrc
ln -s ~/.vim/gvimrc ~/.gvimrc
```

## Switch to the `~/.vim` directory, and fetch submodules:

```sh
cd ~/.vim
git submodule init
git submodule update
```

## Upgrading all bundled plugins

You can use the **foreach** command to execute any shell script in from the root of all submodule directories. To update to the latest version of each plugin bundle, run the following:

```sh
git submodule foreach git pull origin master
```