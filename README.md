# Dotfiles
The setup i personally use on my laptop. \
awesomewm config from https://github.com/Crylia/crylia-theme with a few adjustments. (didn't fork bc i forgot to do that when i made this repo (im to lazy to remake) and this is just a personal setup for me anyway)

ZSH theme is (adjusted) from https://github.com/romkatv/powerlevel10k

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
### Important dependencies
- picom-git
- awesome-git
- rofi-git
- pulseaudio
- probably more i forgot: see https://github.com/Crylia/crylia-theme
  
### Optional/replacable dependencies
- spotifyd
- spotify-tui
- cava (just a sound visualiser)
- alacritty
- thunar
- upower (for power widgets)
- bluez (bluetooth)
- xorg-setxkbmap (to set keyboard layout)
- ttf-meslo-nerd-font-powerlevel10k terminalfont (required by powerlevel10k ZSH theme)
  
### Steps
**Install dependencies:** (exclude any optionals you don't want)\
  for arch: \
  yay -S picom-git awesome-git rofi-git spotify-tui cava \
\
  sudo pacman -S spotifyd pulseaudio pulseaudio-alsa alacritty thunar ly papirus-icon-theme upower bluez bluez-utils playerctl ttf-meslo-nerd-font-powerlevel10k
\
**Git clone and copy into config folder:** \
  git clone https://github.com/Jul-Wie/dotfiles \
  cp -r dotfiles/.config/awesome ~/.config/. \
  cp -r dotfiles/.config/alacritty ~/.config/. \
  cp -r dotfiles/.config/picom.conf ~/.config/. 

**Set up ly as display manager:**
  **Delete or disable whatever dm you do have installed:** \
  For lightdm for example: \
  sudo pacman -Rs lightdm \
  or \
  sudo systemctl disable lightdm \
\
  **then enable ly:** \
  sudo systemctl enable ly \
If that doesn't work check https://github.com/fairyglade/ly
### Main differences from crylia-theme
- In my opinion more intuitive keybindings
- No bottom dock since all open apps are visible in the top bar and opening apps can be done through rofi, so it's basically useless and annoying to manually configure
- Slightly different top bar set-up including working wifi (using  the systray widget which was already included in crylia-theme but used exclively for wifi so there's actually a menu to connect to wifi networks)
- Included startup apps (just picom for me) in startup in rc.lua and deleted separate startup script
- Use of more lightweight ly theme rather than lightdm
- IMO better and more usable alacritty config
  
