# Notes

TODO: How to have this magically updated via Chezmoi

```sh
sudo nano /etc/wsl.conf
```

```txt
[boot]
systemd=true

[network]
# Fixes likely issues with DNS resolution, but YMMV if special DNS is required
generateResolvConf = false

[interop]
# Speeds up autocomplete
appendWindowsPath = false
```
