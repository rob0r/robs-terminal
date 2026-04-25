# Robs terminal ansible

This ansible configures my terminal

I'm using and testing this on

 - Ubuntu 26.04 headless via SSH
 - Windows 11 / WSL2 Ubuntu 26.04 - Windows Terminal
 - MacOS 15 - iTerm2

----------
## Setup

### Prerequisites
Ensure a font from https://www.nerdfonts.com/font-downloads is used for your terminal (starship.rs prereq)

### Ubuntu 26.04
    sudo apt update && sudo apt upgrade -y
    sudo apt install ansible
    git clone https://github.com/rob0r/robs-terminal.git
    cd robs-terminal
    ansible-playbook robsenv.yaml --ask-become-pass

    # sudo.rs doesnt behave with ansible-playbook 
    # https://bugs.launchpad.net/ubuntu/+source/rust-sudo-rs/+bug/2122414
    # https://github.com/ansible/ansible/issues/85837
    ansible-playbook robsenv.yaml --ask-become-pass -e ansible_become_exe=/usr/bin/sudo.ws

### MacOS 15
    brew install ansible
    git clone https://github.com/rob0r/robs-terminal.git
    cd robs-terminal
    ansible-playbook robsenv.yaml

----------
### Style
Working towards green ansible-lint runs however sometimes a little # noqa magic is the only path forward :)
