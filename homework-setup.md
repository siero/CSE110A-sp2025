---
title: "Homework Setup"
layout: single
classes: wide
---
In order for your homeworks to be graded, they must run on the Docker image, which will 
have the same environment as our teaching servers. We will use the image from CSE113 
(Winter Quarter 2023) for this class. This is an introduction to setting up Docker. 
Please let us know if you have other references that you think could be useful!

**The Docker image has a very simple Ubuntu OS. If you use a linux/MacOS/WSL environment 
then it will likely work. However, please double check that code works on the Docker image 
just to be sure. If it does not run, then it can't be graded.**

**Please make sure you understand the storage model of Docker as not all storage is persistent! 
It is always a good idea to back up your work in progress, e.g., using git. But please don't 
make your homework git repos public!**

_This write up has been contributed to by several students: Reese Levine, Yanwen Xu, 
Neal Chokshi, and Devon McKee; please let me know if you have any other suggestions!_

------

## Install Docker

Follow instructions [here](https://docs.docker.com/get-docker/). The desktop version is 
recommended. The following instructions outline how to use Docker primarily through the 
CLI, but the desktop app provides the same functionality and may be easier to use.

## Download the Container

After installing Docker, run the following command: 

```
docker pull reeselevine/cse113:latest   
```

When running, the container includes everything necessary for the homework to work correctly, 
namely `python3`, C++ compilers, and `make`. It also includes two text editors, 
`vim` and `emacs`. If you’d like another text editor included in the image, please let us know.

## Development

Homework skeletons will be included in your created GitHub Classroom repository. 
Clone the homework repository locally. You can either work on your code outside the container, 
using a text editor or IDE of your preference, or you can work on your code inside the container 
using a terminal based text editor like vim or emacs.

There is good support for Docker-VSCode integration using the 
[Dev Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) 
extension. This allows you to hook into the Docker environment within VSCode, letting you access 
files and the terminal just as you would on your host system.

When you’re ready to create the container **make sure you’re in the top level homework directory** 
When you mount this directory within docker the permissions will change, so make sure you aren't 
in a directory that you don't want to lose access to. Once you are ready, run the following 
command depending on your system:

### On Linux/macOS
```
docker run --name cse110a -v "$(pwd)":/assignments -it reeselevine/cse113:latest bash
```

### On Windows 

With Powershell (should work on both [Powershell 7](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.2) and Windows Powershell):

```
docker run --name cse110a -v ${pwd}:/assignments -it reeselevine/cse113:latest bash
```

With cmd (Command Prompt): 

```
docker run --name cse110a -v %cd%:/assignments -it reeselevine/cse113:latest bash
```

You should be running inside the container at this point. Running `ls` should list your files. 
At any point, to exit the container just type `exit`. Once you exit the container you can re-run 
the existing container either via the Docker Desktop UI by clicking the "run" icon within the 
list of available containers, or by running the following command in a terminal/powershell/cmd instance:

Start the container with `docker start cse110a`: Add `-i` if you want an interactive shell. 
Once the container has started, you can use the shell if you passed `-i`, or you can connect 
to the container in VSCode.

```
docker start cse110a -i
```

At this point, you can edit your code and run it by following the instructions on the homework. 
Any changes you make to your files inside the container will persist when the container exits.

We recommend keeping your homework files under source control using git or another tool, since 
this will help with keeping track of your changes and making sure you don’t lose your work.

## More Details About Docker

While the details of running Docker containers are unnecessary for this course, it might be helpful 
to understand what each part of the above commands are doing.

* `docker pull` downloads the specified image, which in this case is 
`reeselevine/cse113:latest`, where `reeselevine/cse113` is the image name and latest is 
the tag. Docker allows multiple tags for the same image, but for this course we will most 
likely only be using the default latest tag for images.

* `docker run` is a command to both create and start a container.

* `docker start` lets you start a container that has already been created

* `-v` mounts a volume from the host (your computer) to the Docker container. We are mounting the 
current host machine directory to the directory `/assignments` inside the container.

* `-it` gives us an interactive, terminal based session. Without this, the container would immediately exit.


## Useful Docker commands

* `docker container prune`: Each `docker run` execution creates a new container, it will stop when you exit. 
**Do not create a new container each time you want to work on your project**. Using `docker run` for 
the initial setup and then exiting and calling `docker start` whenever you want to resume development 
is the recommended workflow. Having a bunch of Docker containers can take a lot of space, fast. Some time 
it is useful to prune all stopped containers by running `docker container prune` to gain some space. 

