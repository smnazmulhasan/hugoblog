+++
title = 'How to Connect Wi Fi in Vanilla Arch'
date = 2024-01-25T22:13:17+06:00
draft = false
categories = ["Linux", "Archlinux"]
tags = ["linux", "archlinux", "wifi", "networkmanager", "screenshot"]
+++

![alt](/images/archlinux.jpg)

Connect wifi during installation

```
wpa_supplicant -B -i wlan0 -c <(wpa_passphrase "ssid" "passphrase")
```

### Conntect WiFi on first boot
__N.B: Required Network Manager__
```
nmcli device wifi connect Your_SSID password Your_Password
```
