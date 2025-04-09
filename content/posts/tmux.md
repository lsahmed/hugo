---
title: "Tmux : Terminal Multiplexers"
date: 2025-04-08
# weight: 1
# aliases: ["/first"]
tags: ["devops"]
author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false

hidemeta: false
comments: false
description: "I figured out about tmux from an online article, so I started learning it."
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/lsahmed/hugo/tree/main/content/"
    Text: "Suggest Changes" # edit text 
    appendFilePath: true # to append file path to Edit link
---

## Why to learn Tmux?
So, the main and important question to ask is: why use Tmux? If I can do all my work from a single terminal, then
why would I even touch it?

Because Tmux is a terminal multiplexer — it allows you to create several "pseudo-terminals" from a single terminal. This is very useful for running multiple programs with a single connection, such as when you're remotely connecting to a machine using Secure Shell (SSH).

## Installing Tmux 🚀
The first step is to install it on your machine, because without it, you obviously can’t use it.

### ForLinux 
#### Debian Based
Install it with ```apt``` package manager.

```bash
  sudo apt install tmux
```
#### Arch Linux
Install it with ```pacman``` package manager simply.

```bash
  pacman -S tmux
```
#### For Fedora 
Install it with ```dnf```.

```bash
  dnf install tmux
```
#### For RHEL or CentOS 
Install it with ```yum```.

```bash
  yum install tmux
```

### For MacOs
Just use the homebrew package manager to install it. (recommended way)
```bash
    brew install tmux
```

### For Windows
Unfortunately, there’s no official package available for Windows.
However, you can install it using WSL (Windows Subsystem for Linux) and follow the Linux guide.

## Basic Concepts of Tmux 🛰️
Before really starting to use tmux one must understand the basic things that are important to control tmux.

### Some Keywords to memorize
| Keyword | Description / Use Case                                                                 |
|---------|------------------------------------------------------------------------------------------|
| Session | A Tmux session is like a workspace. You can create multiple sessions and switch between them. Useful for managing different projects or tasks. |
| Window  | Each session can have multiple windows (like tabs). A window typically runs one shell or program. |
| Pane    | A window can be split into multiple panes. Each pane is like a mini-terminal within the window. Great for multitasking or monitoring multiple processes. |
| Status Bar | The status bar is the line at the bottom of the Tmux interface. It shows info like session name, windows, time, and can be customized with plugins or scripts. |

## Let's Use Tmux
After successfully installing tmux open your terminal and type 
```bash
  tmux
```
- This will start a new tmux session without a special name.

To start a tmux session with a name of your choice you can use the ```-s``` flag.
```bash
  tmux new -s desired_name
```
This will open a session in your terminal. You can see your session name at the bottom of your session. This bottom bar is known as the Status Bar.

![Sample photo](https://i.ibb.co/20FwQ5pv/Screenshot-2025-04-08-at-6-15-04-PM.png)
Like in the photo above, you'll be able to see something similar.

### Key Bindings to remember 

#### For controlling panes
| Key Binding        | Use Case                                                                                        |
|-------------------------|-------------------------------------------------------------------------------------------------|
| ```Ctrl + B + %```      | To create a pane horizotally within the window of the session.|
| ```Ctrl + B + "```      | To create a pane vertically within the window of the session.|
| ```Ctrl + B + ⬆️⬅️➡️⬇️```| To navigate among the panes.|

![Three panes](https://i.ibb.co/N6nsVK9p/three.png)
