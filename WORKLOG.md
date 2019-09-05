# Notes on Kubernetes on Pi

Basic info: https://medium.com/nycdev/k8s-on-pi-9cc14843d43

## 20190829 - Set up SD cards 

Install Etcher (balenaEtcher) (https://www.balena.io/etcher/) on laptop (laptop is my Windows PC)

Download lite version of raspbian from https://www.raspberrypi.org/downloads/raspbian/ - Raspbian Buster Lite

### Main card
Flash image onto 64Gb SDHC card with Etcher.

Add empty ssh file onto newly flashed card (will provide ssh access)

### Each slave card
Flash image onto 32Gb SDHC card with Etcher.

Add empty ssh file onto newly flashed card (will provide ssh access)

## 20190905 - Basic setup of all PIs with tmux

### Install tmux on windows

0) Make sure git is installed including git bash.  Follow https://blog.pjsen.eu/?p=440 (How to run Tmux in GIT Bash on Windows)
1) Install https://www.msys2.org and start it (pacman) 
2) `pacman -Syu` `pacman -Su` `pacman -S git` to update
3) `pacman -S tmux` to install tmux
4) Copy tmux.exe and msys-event-2-1-4.dll (version may vary) from `<msys2-folder>\usr\bin` to your Git for Windows directory, i.e. C:\Program Files\Git\usr\bin. 

You can now run Tmux in Git Bash by simply typing `tmux`.  Cheat sheet:

```
CTRL+B, (release and then) C — create new shell within existing terminal window
CTRL+B, N — switch between shells
CTRL+B, a digit — switch to the chosen shell by the corresponding number
CTRL+B, " — split current window horizontally into panels (panels are inside windows)
CTRL+B, o — switch between panels in current window
CTRL+B, x — close panel
```
### Configuring the Raspberry Pis 

Follow basic guide again.  Insert SD cards in Raspberry Pis and connect to router.



