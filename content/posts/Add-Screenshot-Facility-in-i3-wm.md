+++
title = 'Add Screenshot Facility in I3 Wm'
date = 2024-01-25T23:12:42+06:00
draft = false
categories = ["Linux", "i3wm"]
tags = ["linux", "archlinux", "i3", "i3wm", "screenshot"]
+++

__Dependencies:__  maim, xclip, xdotool

```bash
##  Screenshots in files
bindsym Print exec --no-startup-id maim --format=png "/home/$USER/Pictures/screenshot-$(date -u +'%Y%m%d-%H%M%SZ')-all.png"
bindsym $mod+Print exec --no-startup-id maim --format=png --window $(xdotool getactivewindow) "/home/$USER/Pictures/screenshot-$(date -u +'%Y%m%d-%H%M%SZ')-current.png"
bindsym Shift+Print exec --no-startup-id maim --format=png --select "/home/$USER/Pictures/screenshot-$(date -u +'%Y%m%d-%H%M%SZ')-selected.png"

## Screenshots in clipboards
bindsym Ctrl+Print exec --no-startup-id maim --format=png | xclip -selection clipboard -t image/png
bindsym Ctrl+$mod+Print exec --no-startup-id maim --format=png --window $(xdotool getactivewindow) | xclip -selection clipboard -t image/png
bindsym Ctrl+Shift+Print exec --no-startup-id maim --format=png --select | xclip -selection clipboard -t image/png
```
