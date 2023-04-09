---
title: Terminal customization
author: meyer
date: 2023-03-14 20:04:00 -0500
categories: [Tutorial]
tags: [linux, terminal, kitty]
---

To have a user-friendly terminal, we need to use software that help us with this task, in this article you will learn how to get a beautiful and very customizable terminal on linux, note that it can take a long.

#### Fonts

To see icons on our terminal with need to use a compatible font, for this porpuse you can use HackNerdFont, to download this font just [click here](https://about:blank), then unzip it to system folder fonts.

```shell
sudo mkdir /usr/share/fonts/HackNerdFont
unzip ~/Downloads/HackNerdFonts.zip -d /usr/share/fonts/HackNerdFont
```

### Kitty

For the terminal we'll use Kitty, this can be download from de [official site](https://sw.kovidgoyal.net/kitty/) or with some package manager like `apt`.
```shell
sudo apt update
sudo apt install kitty -y
```

Let's create the config file.

```shell
touch ~/.config/kitty/kitty.conf
```

Now add the following settings to the file.

```conf
# Disable bell
enable_audio_bell no

# Font
font_family HackNerdFont
font_size 12
url_color #61afef

# Keyboard shortcuts
## Move through windows
map ctrl+left neighboring_window left
map ctrl+right neighboring_window right
map ctrl+up neighboring_window up
map ctrl+down neighboring_window down

## Suspend work
map ctrl+shift+z toggle_layout stack

## New window/tab
map ctrl+shift+enter new_window_with_cwd
map ctrl+shift+t new_tab_with_cwd

# Cursor
cursor_shape beam
cursor_beam_thickness 1.8

# Mouse
mouse_hide_wait 3.0
detect_urls yes

# Input
repaint_delay 10
input_delay 3
sync_to_monitor yes

# Tabs
tab_bar_style powerline
inactive_tab_background #e06c75
active_tab_background #98c379
inactive_tab_foreground #000000

# Window
background_opacity 0.95
window_padding_width 4

# Default shell
shell zsh

```
{: file='~/.config/kitty/kitty.conf'}

### ZSH

To have a beautiful terminal, we need to use a zshell so let's download.

```shell
sudo apt install zsh -y
```

### PowerLevel10K

![PowerLevel10K](https://raw.githubusercontent.com/romkatv/powerlevel10k/powerlevel10k.png){: width="972" height="589" }
_PowerLevel10K makes zsh better_

### Plugins

#### FZF

### NVIM

#### NVCHAD
