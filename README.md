# Windows Terminal - Setup

This repository contains my setup for the [Windows Terminal](https://en.wikipedia.org/wiki/Windows_Terminal), as I almost exclusively use WSL on Windows and find the built-in terminals for WSL, Python, Powershell, and CMD really ugly and cumbersome.

- Shells/Profiles
    - Defaults to Ubuntu-20.04 ([must be installed with WSL](https://docs.microsoft.com/en-us/windows/wsl/install#install)).
    - Python
    - Powershell
    - CMD
- Global keybindings
    - Similar to the ones I use on [VSCode](https://github.com/lu0/vscode-settings).
        - Tab navigation
        - Pane navigation/resizing
        - Etc.
- Color Scheme
    - Similar to the ones of [my Linux Dotfiles](https://github.com/lu0/dotfiles_linuxMint#terminal) and [my VSCode theme](https://github.com/lu0/vscode-theme-interplanetary-craft).
- Font
    - [Source Code Pro](https://github.com/adobe-fonts/source-code-pro) (must be installed).
- Prompt (WSL profiles only)
    - [My variation of Fancy Bash](https://github.com/lu0/dotfiles_linuxMint/blob/master/bash/fancy-bash.sh) (must be installed within the WSL distro).

![Windows Terminal using my settings](assets/windows-terminal-custom.png)

## Install
Close the Windows Terminal if it's open, then go to the Windows Terminal's settings folder:
```sh
cd /mnt/c/Users/<YOUR_WINDOWS_USER>/AppData/Local/Packages/Microsoft.WindowsTerminal_8wekyb3d8bbwe
```

Clone the repository under `LocalState`
```sh
git clone https://github.com/lu0/windows-terminal-setup LocalState
```
