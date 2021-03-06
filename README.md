# Dev configurations for Ubuntu
Configuration parameters used on the different linux applications. My personal set up.

![Screenshot](http://i.imgur.com/xXjk0NV.png)


## Unity tmux shortcut

First thing, copy .termric.sh to your home folder or whatever location you feel suitable, this path should be updated on 
the tmux.desktop file.

Copy tmux.desktop to your /usr/share/applications/ folder, keep in mind you need sudo permission to do so. 

The new app icon will be displayed on unity after reloading its database with:

	sudo update-desktop-database


## Ubuntu Icons and theme

Just add the numix repository running the following commads

	sudo add-apt-repository ppa:numix/ppa
	sudo apt-get update
	sudo apt-get install numix-gtk-theme numix-icon-theme-circle

Then you'll need to instal Unity Tweak Tool: 
	
	sudo apt-get install unity-tweak-tool

Run the tweak tool and pick Numix as theme



## Gnome Terminal Theme

Run ./base16-monokai.dark.sh this will add a new profile on your terminal emulator. 
These scripts were made by [Chris Kempson](https://github.com/chriskempson/base16-gnome-terminal)

>Preferred font so far: DejaVu Sans Mono Book


## OhMyZsh

**Installing zsh:**

	sudo apt-get update
	sudo apt-get install zsh

**PowerLine FONTS**

Must have for some OMZSH themes (Cute icons 'n stuff)

	wget https://github.com/Lokaltog/powerline/raw/develop/font/PowerlineSymbols.otf https://github.com/Lokaltog/powerline/raw/develop/font/10-powerline-symbols.conf
	sudo mv PowerlineSymbols.otf /usr/share/fonts/
	sudo fc-cache -vf
	sudo mv 10-powerline-symbols.conf /etc/fonts/conf.d/

**Installing Oh my zsh** (This requires you to have Git)
	
	sudo curl -L http://install.ohmyz.sh | sh

Execute zsh for the first time and select the recommended option (The one that creates the .zshrc with default values)
Then edit the ZSH_THEME parameter on your ~/.zshrc file replacing it with "xiong-chiamiov-plus"
	
	ZSH_THEME="xiong-chiamiov-plus"  

or download honukai.zsh-theme from [Oskarkrawczyk](https://github.com/oskarkrawczyk/honukai-iterm-zsh)
and place it on your `~/.oh-my-zsh/themes/` folder, then change your ZSH_THEME parameter
	
	ZSH_THEME="honukai"

## Tmux

First of all install tmux

	sudo apt-get update
	sudo apt-get install tmux

Then copy/replace the .tmux.conf file of your home directory with the one on this repository (tmux/.tmux.conf)

> **NOTE:** Tmux mouse support is enabled on the configuration file, therefore you have to hold *Shift* key to select text on the terminal. To disable this remove *set -g mouse on* from the configuration file.


## Vim

Copy the folder colors to your ~/.vim/ folder (Create it in case you don't have it) then copy .vimrc file to your home directory. In case you have one, just update its content with the one provided.



	



