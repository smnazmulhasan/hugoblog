+++
title = 'How to Show WiFi Password in Windows'
date = 2024-02-05T14:16:15+06:00
draft = false
categories = ["Tricks", "WiFi Hack"]
tags = ["wifi", "password-hack", "windows", "windows10", "win10wifi"]
+++

Youy go to a friends house and want to know his wifi password without asking him?
If your friend has a windows pc and you have access to it for just 10 seconds then you are lucky.

## Wifi password showing tricks with windows cmd

copy below code and paste it to a notepad and save it as a "Anything.cmd" file

```cmd
@echo off
 color 0a
 title Intel.dll
 netsh wlan show profile "YOUR_WIFI_SSID" key=clear >Pass.txt
```
Then run it by double clicking the ".cmd" file. You will find a file in called "Pass.txt" Open the file and there you will find the wifi password.
