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
