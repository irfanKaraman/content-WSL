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
cd /mnt/c/users/irfan/documents  #access host windows from linux cli
touch test.txt //create file
mkdir test //create folder
sudo mv source_path target_path //move file/folders from source to target destination
sudo apt update //update linux
sudo apt install APP //install app-package on linux
```

# Install nodeJS on Linux
```
  curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash - &&\
  sudo apt-get install -y nodejs
```
- Check here for updates > https://github.com/nodesource/distributions#debinstall

# main.nodeJS Codes
```
var http = require('http');

http.createServer(function (req, res) {
    res.write('NODE JS SUNUCUSU OK');
    res.end();

}).listen(9000); 
```

# index.nodeJS Codes
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

- Check server state from linux cli
 ```
 curl -i http://localhost:9000
```
