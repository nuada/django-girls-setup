# Django Girls

## Prerequisites

### Install Chocolatey

Run PowerShell as Administrator and execute commands:
```
Set-ExecutionPolicy remotesigned
iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

### Install tools
As Administrator execute in shell:
```
choco install python
choco install git
choco install visualstudiocode
```

### Install Docker
On Windows 10+:
```
choco install docker-for-windows
```
On Window 7/Vista download and install: [Docker Toolbox](https://github.com/docker/toolbox/releases/tag/v1.12.3).

### Install Visual Studio Code plugins
 * Python
 * Django Template
 * vscode-flake8

 Plugin dependencies will be pulled in automatically (vscode will ask, just allow it to proceed).

### Setup Docker
You can use vscode built-in terminal `View -> Integrated terminal` to create Docker container:
```
docker run -it -v /c/Users/<username>/Desktop/django-girls:/django-girls --name django-girls -p 8000:8000 python bash
```

Inside container update `pip` and install Django:
```
pip install --upgrade pip
pip install django~=1.9.0
apt-get update
apt-get install vim-nox
```

If you close (or stop) your container you can restart it using command:
```
docker start django-girls
```

To start using previously created container you need to attach you terminal:
```
docker attach django-girls
```

To run command when Django server is running you can open new shell inside container using:
```
docker exec -it django-girls bash
```

When using terminal with Docker container follow instructions for Linux.

## Django and Docker
From your computers' point of view Docker container looks like separate machine. When runing Django inside container remember to use IP and port accessible from outside:
```
./manage.py runserver 0:8000
```