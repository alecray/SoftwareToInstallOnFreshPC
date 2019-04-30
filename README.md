# Software To Install On A Fresh PC
When I get a new PC, these are all the things I typically install first:
* Google Chrome
* Git (& `git lola`)
* VIM (comes with Git for Windows)
* Slack 
* Blender
* Core Temp
* Search Everything
* OBS Studio
* Sublime Text 3
* MailBird
* Logitech Gaming Software
* Steam
* VLC Media Player

### To Do:
* Update Drivers (Windows Update)
* Update Graphics (GeForce Experience)
* OhMyWindows! (OhMyFish for Windows)
* To install Ubuntu Subsystem:
1. Type "Developer Mode" in Start Menu, tick "Developer Mode"
2. Type "Windows Features" in Start Menu, scroll down and tick "Windows subsystem for Linux (Beta)"
3. Restart Computer
4. Go to Microsoft Store, install Ubuntu
  
### To install OhMyFish, Fishshell and TMUX
1. sudo apt-get install fish
2. Make fish default shell by running `vim ~/.bashrc`
3. Somewhere near the top, put this:
``` 
if [ -t 1 ]; then
    exec fish
fi
```
4. curl -L http://get.oh-my.fish | fish
5. Install an OMF theme using `omf install theme_name`
6. Install tmux with `sudo apt-get install tmux`
7. Run `vim ~/.local/share/omf/init.fish` and put this somewhere (near bottom after function is what I did):
```
if status is-interactive
and not set -q TMUX
    exec tmux 
end
```
8. Use [this article](https://www.hamvocke.com/blog/a-guide-to-customizing-your-tmux-conf/) to make TMUX usable.
