# Robs terminal ansible

This ansible aims to keep terminal things as consistent as possible between WSL2 Ubuntu and MacOS

I'm using and testing this on

 - Windows 11 / WSL2 Ubuntu 24.04 - Windows Terminal
 - MacOS 15 - iTerm2

----------
## Setup

### Prerequisites
ensure a font from https://www.nerdfonts.com/font-downloads is used for your terminal (starship.rs prereq)

### WSL2 Ubuntu 24.04
    sudo apt update
    sudo apt upgrade -y
    sudo apt install ansible
    git clone https://github.com/rob0r/robs-terminal.git
    cd robs-terminal
    ansible-playbook robsenv.yaml --ask-become-pass

### MacOS 15
    brew install ansible
    git clone https://github.com/rob0r/robs-terminal.git
    cd robs-terminal
    ansible-playbook robsenv.yaml

----------
### Style
Working towards green ansible-lint runs however sometimes a little # noqa magic is the only path forward :)
