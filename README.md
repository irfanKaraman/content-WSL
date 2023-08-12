# 01 - Tech Talks | DevOps Series
> Ubuntu/Linux & Git & VScode & NodeJS Installation and Configuration on WSL2 with Windows Terminal (Windows 11 OS)


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


# Linux/Ubuntu Commands

```
cd /mnt/c/users/irfan/documents  //access host windows from linux cli
touch test.txt //create file
mkdir test //create folder
sudo mv source_path target_path //move file/folders from source to target destination
sudo apt update //update linux
sudo apt install APP //install app-package on linux
```


# vsCode Download Link
> https://code.visualstudio.com/


# Git Bash Download Link
> https://gitforwindows.org/


# Git Commands

```
  git init //initialize git
  sudo apt install gitsome //install gitsome for autocomplete commands
  git config --global user.email xyz@xyz.com
  git config --global user.name Jane Doe
  git clone https://USERNAME:TOKEN@github.com/USERNAME/REPONAME.git
  git remote set-url origin https://USERNAME:TOKEN@github.com/USERNAME/REPONAME.git //Should be on git repo folder
  git add . //add all files
  git add README.txt //add specific file
  git commit -m "commit" //commit
  git push -u origin master //push
  git status //status check
  git fetch
  git pull origin
```


# Install nodeJS on Ubuntu

```
  curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash - &&\
  sudo apt-get install -y nodejs
```
- Check here for updates > https://github.com/nodesource/distributions#debinstall


# nodeJS Commands for Ubuntu

```
npm init -y  //initialize
npm install express 
node main.js //run the code
```


# main.nodeJS 

```
var http = require('http');

http.createServer(function (req, res) {
    res.write('NODE JS SERVER WORKING');
    res.end();

}).listen(9000); 
```


# index.nodeJS 

```
var http = require('http');
var url = require('url');

http.createServer(function (req, res) {
  res.writeHead(200, {'Content-Type': 'text/html'});
  var q = url.parse(req.url, true).query;
  var txt = q.year + " " + q.month;
  res.end(txt);

}).listen(8000);
```

- Check server state from ubuntu cli
```
 curl -i http://localhost:PORT
```





