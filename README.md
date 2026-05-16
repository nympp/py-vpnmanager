<span id="top"></span>

<div align="center">
    <img src="https://github.com/nympp/py-vpnmanager/blob/main/pywg-icon.png?raw=true" width=60px height=60px>
    <h1>pyWG-GUI</h1>
    <p>python Wireguard GUI is a GUI for Wireguard on Linux systems. Built with python and TkInter module.</p>
</div>

## Table of contents
- [How to install](#how-to-install)
    - [Requirements](#requirements)
    - [Installation](#installation)
    - [Optional: Use it anywhere](#optional--use-it-anywhere)
- [Usage](#how-to-use)

## How to install

### Requirements
- Python
- Python TkInter package
- Tk package on your system

### Installation

First, download the source code
```bash
git clone https://github.com/nympp/pywg-gui.git
```

Then move the directory `pywg-gui` to your desired location
```
mv pywg-gui ~/Documents/my-folder/
```

Then open manager.py with your prefered text editor and edit these lines :
```python
# MANAGER_INSTALL_PATH is where you moved the pywg-gui folder
MANAGER_INSTALL_PATH = "/home/user/Documents/my-folder/pywg-gui"
# BASE_OPEN_PATH is where you want the program to start when you want to select a file (the popup will open on the folder you will put here)
BASE_OPEN_PATH = "/home/user/Downloads"
```

The program is ready! You can start it with : 
```bash
python manager.py
```

### Optional : Use it anywhere
- [Alias in bashrc](#option-1--use-a-alias-in-bashrc-or-fishsh-equivalent)
- [File in /bin](#option-2--use-a-file-in-bin)
- [Desktop entry](#option-3--add-a-desktop-entry)

#### Option 1 : Use a alias in .bashrc (or fish/sh equivalent)

```bash
nano ~/.bashrc
```
Add the following line with your install path :
```bash
alias pywg="python /home/user/Documents/my-folder/pywg-gui"
```
Then restart bash, you can now do :
```bash
pywg
```
and it will open the GUI!

#### Option 2 : use a file in /bin

```bash
sudo touch /bin/pywg && sudo chmod +x /bin/pywg
sudo nano /bin/pywg
```

Add this line :
```bash
python /home/user/Documents/my-folder/pywg-gui
```

You can now do (in most systems) :

```bash
pywg
```

#### Option 3 : Add a desktop entry

```bash
cd ~/.local/share/applications
touch pywg.desktop && chmod +x pywg.desktop
```

```bash
nano pywg.desktop
```

Add the following :

```desktop
[Desktop Entry]
Name=pyWG GUI
Exec=python /home/user/Documents/my-folder/pywg-gui/manager.py
Terminal=false
Type=Application
Icon=/home/user/Documents/my-folder/pywg-gui/pywg-icon.png
Comment=python Wireguard GUI
Categories=Utility;
```

## How to use

Coming soon

---
[Go back to top](#top)