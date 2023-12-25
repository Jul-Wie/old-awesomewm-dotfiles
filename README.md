# Dotfiles
This repo contain the dotfiles i use on my laptop, so it's all lightweight stuff.
I stole my awesomewm config from https://github.com/Crylia/crylia-theme and made a few adjustments.


## List of stuff
- OS: arch based
- DM: ly
- WM: awesome-git
  
- Music: spotify-tui + spotifyd
- Browser: librewolf
- Cloud sync: rclone
- Documents: libreoffice
- File manager: Thunar
- Term: Alacritty
- Compositor: picom-git

## Setup/Installation

### Main differences from crylia-theme
- In my opinion more intuitive keybindings
- No bottom dock since all open apps are visible in the top bar and opening apps can be done through rofi, so it's basically useless and annoying to manually configure
- Slightly different top bar set-up including working wifi (using  the systray widget which was already included in crylia-theme but used exclively for wifi so there's actually a menu to connect to wifi networks)
- Included startup apps (just picom for me) in startup in rc.lua and deleted separate startup script
  
