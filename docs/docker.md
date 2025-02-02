# Docker Setup for Personal Machines

## Initial Setup

### Windows

1. Install Docker ([Windows 10](https://download.docker.com/win/stable/Docker%20for%20Windows%20Installer.exe), [Windows 7 or 8](https://docs.docker.com/toolbox/toolbox_install_windows/)) Note: During the installation *don't* check the "Use Windows containers..." box.
2. Run Docker Desktop. (You may get a message about Hyper-V and Containers that will require a reboot, press "Ok" and wait through several reboots.)
3. Run Windows PowerShell and the application instructions below. (You may get a message about sharing your C:\ drive with Docker, accept.)

### macOS

1. Install Docker ([macOS 10.12 or newer](https://download.docker.com/mac/stable/Docker.dmg), [macOS 10.8 to 10.11](https://docs.docker.com/toolbox/toolbox_install_mac/).
2. Run Terminal (/Applications/Utilities/Terminal) and the application instructions below.

### Linux

1. [Install Docker](https://docs.docker.com/install/) via distribution specifc instructions.
2. Run Terminal and the application instructions below.

### Note About Initial Download of the Images

The intial run of the image will also download the latest copy of the image to your machine. We have copies of the images locally and can assist with their installation as this method will likely be much faster than downloading.

## R with RStudio

### Windows

1. In Windows PowerShell run: `docker run --name tph --rm -p 127.0.0.1:8787:8787 -v ${HOME}:/home/rstudio -e DISABLE_AUTH=true thinkplayhack/r_rstudio:latest` .
2. Go to [127.0.0.1:8787](http://127.0.0.1:8787) in a web browser.

### macOS & Linux

1. In Terminal run: `docker run --name tph --rm -p 127.0.0.1:8787:8787 -v ${HOME}:/home/rstudio -e DISABLE_AUTH=true thinkplayhack/r_rstudio:latest`.
2. Go to [127.0.0.1:8787](http://127.0.0.1:8787) in a web browser.

## Python with Jupyter

### Windows

1. In Windows PowerShell run: `docker run --name tph --rm -p 127.0.0.1:8888:8888 -v ${HOME}:/home/jovyan thinkplayhack/python_jupyter:latest`.
2. Go to [127.0.0.1:8888](http://127.0.0.1:8888) in a web browser.

### macOS & Linux

1. In Terminal run: `docker run --name tph --rm -p 127.0.0.1:8888:8888 -v ${HOME}:/home/jovyan thinkplayhack/python_jupyter:latest`.
2. Go to [127.0.0.1:8888](http://127.0.0.1:8888) in a web browser.

