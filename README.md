# content-wsl
activate and install wsl, ubuntu, vscode.


# Activate & Install WSL
- Windows Feature enable Hyper-v + Windows Subsystem for Linux
- Also you can install via Powershell (make sure it is running as Admin)
  ```
  wsl.exe --install
  wsl --version
  wsl --update
  ```
# Install Windows Terminal
- Windows Store
- Also you can install from Github > https://github.com/microsoft/terminal/releases

# Install Linux on WSL
- Windows Store
- Also you can install from Windows Terminal
```
  wsl --list --online
  wsl --install -d ubuntu-20.04
```

# WSL Commands

```
  wsl --update
  wsl --shutdown //turn of all machines
  wsl -t Ubuntu-20.04 //turn of only specified machine
  wsl -l -v
  wsl --update
```

# Linux Commands
```
cd /mnt/c/users/irfan/documents  //access host windows from linux cli
touch test.txt //create file
mkdir test //create folder
sudo mv source_path target_path //move file/folders from source to target destination
sudo apt update //update linux
sudo apt install APP //install app-package on linux
```

# Install nodeJS
https://github.com/nodesource/distributions#debinstall
```
  curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash - &&\
  sudo apt-get install -y nodejs
```


```
#Oh-my-zsh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
brew install font-hack-nerd-font
```

## Other Tools



### Re-read config
```
:source-file ~/.tmux.conf
```
