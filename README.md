# asahi
Asahi Linux Notes and Scripts

## Switch Fn and Control Buttons
```
# /etc/modprobe.d/hid_apple.conf
options hid_apple swap_fn_leftctrl=1
```
Then run:
```
sudo dracut --regenerate-all --force
```

## Install Docker
```
sudo dnf install docker docker-compose
sudo systemctl enable docker
sudo systemctl start docker
```

## Install Node
```
sudo dnf install nodejs
```

## Enable global clipboard from terminal apps
```
sudo dnf install wl-clipboard
```

## Enable deps for BeeKeeper AppImage
```
sudo dnf install zlib-devel fuse
```
Then make desktop file
```
# ~/.local/share/applications/beekeeper.desktop
[Desktop Entry]
Name=Beekeeper Studio
Exec=/home/mkelly/Beekeeper.AppImage --enable-features=UseOzonePlatform --ozone-platform=wayland
Icon=beekeeper-studio
StartupWMClass=beekeeper-studio
Type=Application
Categories=Utility;Application;
Terminal=false
X-AppImage-Version=1.0
Comment=This is a comment about the AppImage
```

## Git Gui
```
flatpak install flathub com.github.Murmele.Gittyup
```


## Gnome Enable Fractional Scaling
```
gsettings set org.gnome.mutter experimental-features "['scale-monitor-framebuffer']"
```

## Gnome Tweaks and Dark Legacy Theme
```
sudo dnf install gnome-tweaks gnome-themes-extra
```

## Better Icons
```
sudo dnf install papirus-icon-theme
```

## Install Helix Editor and LSPs
```
sudo dnf install helix
sudo npm install -g vscode-langservers-extracted
sudo npm install -g @tailwindcss/language-server --force
sudo npm install -g intelephense
```

## Gnome Extensions
```
sudo dnf install gnomne-extension-app
```

