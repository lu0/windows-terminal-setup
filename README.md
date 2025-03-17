# Windows Terminal - Setup

This repository contains my configuration for [Windows Terminal](https://en.wikipedia.org/wiki/Windows_Terminal). I created this setup because I primarily use WSL on Windows and found the default terminals for WSL, Python, PowerShell, and CMD lacking in usability and appearance.

![Windows Terminal using my settings](assets/windows-terminal-custom.png)

- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Customization](#customization)
- [Common Issues](#common-issues)

## Features

- **Shells/Profiles**
  - Uses your default WSL distribution
  - Python (within WSL)
  - PowerShell
  - CMD

- **Keyboard Shortcuts**
  - Tab navigation (create, close, switch)
  - Pane management (split, navigate, resize)
  - Clipboard operations
  - Profile switching: 
    - <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>1</kbd> for Linux
    - <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>2</kbd> for Python
    - <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>3</kbd> for PowerShell
    - <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>4</kbd> for CMD
  - Similar to my [VSCode settings](https://github.com/lu0/vscode-settings)

- **Appearance**
  - Color scheme matching [my Linux Dotfiles](https://github.com/lu0/dotfiles_linuxMint#terminal) and [VSCode theme](https://github.com/lu0/vscode-theme-interplanetary-craft)
  - [Source Code Pro](https://github.com/adobe-fonts/source-code-pro) font
  - Custom prompt for WSL using [my Fancy Bash variation](https://github.com/lu0/dotfiles_linuxMint/blob/master/bash/fancy-bash.sh)

## Requirements

- [Windows Terminal](https://github.com/Microsoft/Terminal)
- [Windows Subsystem for Linux (WSL)](https://docs.microsoft.com/en-us/windows/wsl/install#install) with at least one Linux distribution
- [Source Code Pro font](https://github.com/adobe-fonts/source-code-pro/releases) installed on Windows (TTF recommended)
- (Optional) [My Fancy Bash prompt](https://github.com/lu0/dotfiles_linuxMint/blob/master/bash/fancy-bash.sh) for the custom WSL prompt

## Installation

1. Close the Windows Terminal if it's running
2. Open PowerShell
3. Enter WSL with the `wsl` command
4. Go to the Windows Terminal settings folder:
   ```sh
   cd "/mnt/c/Users/$(whoami.exe | cut -d'\' -f2 | tr -d '\r')/AppData/Local/Packages/Microsoft.WindowsTerminal_8wekyb3d8bbwe"
   ```
5. Back up your existing configuration if needed:
   ```sh
   cp -r LocalState LocalState_backup
   ```
6. Remove the default configuration:
   ```sh
   rm -rf LocalState
   ```
7. Clone this repository:
   ```sh
   git clone https://github.com/lu0/windows-terminal-setup LocalState
   ```
8. Exit WSL and PowerShell, then open the Windows Terminal

## Customization

You can edit `settings.json` in the LocalState folder to further adjust the terminal to your needs.

## Common Issues

- If Windows Terminal doesn't load, check for errors in `settings.json`
- For WSL issues, verify your Linux distribution is properly installed
- Font problems usually mean Source Code Pro isn't installed correctly
