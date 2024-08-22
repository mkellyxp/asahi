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
Type=Application
Categories=Utility;Application;
Terminal=false
X-AppImage-Version=1.0
Comment=This is a comment about the AppImage
```


## Gnome Enable Fractional Scaling
```
gsettings set org.gnome.mutter experimental-features "['scale-monitor-framebuffer']"
```

## Gnome Tweaks and Dark Legacy Theme
```
sudo dnf install gnome-tweaks gnome-themes-extra
```
