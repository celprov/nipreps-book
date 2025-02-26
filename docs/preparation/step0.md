# Before we start: How to follow this tutorial

This tutorial contains a mix of lecture-based and interactive components.
The interactive components can be executed in your personal computer locally or using the [Binder](https://jupyter.org/binder) service.
You are welcome to follow along however you like, whether you just want to listen or code along with us.
Each of the chapters involving code are actually Jupyter notebooks!

## <i class="fa fa-rocket" aria-hidden="true"></i> Using Binder

Clicking the Binder icon in the top right corner will launch an interactive computing environment with all of the necessary software packages pre-installed.

This is the easiest and quickest way to get started.

```{figure} ../images/binder_link.png
:name: binder_link

```

````{tip}
At first, the lesson may open as a Markdown file.
You can re-open it as a Jupyter notebook by right-clicking the filename on the right sidebar, clicking "Open With" and finally clicking "Notebook".

```{figure} ../images/convert_notebook.png
:name: convert_notebook

```
````

```{attention}
If using Binder, please be aware that the state of the computational environment it provides is not permanent.
If you are inactive for more than 10 minutes, the environment will timeout and all data will be lost.
If you would like to preserve any progress, please save the changed files to your computer.
```

## <i class="fas fa-hammer"></i> Local installation ("bare-metal")

If you would like to follow along using your own setup and you have a functional Python environment, you can run the following commands in your terminal:

```bash

# 1. clone this repository
git clone https://github.com/nipreps/nipreps-book

# 2. install the necessary python packages in your Python environment
cd nipreps-book && pip install -r requirements.txt

# 3. launch a Jupyter lab instance
jupyter lab

```

The image registration lesson requires an installation of [ANTs](https://github.com/ANTsX/ANTs).
Separate instructions can be found for [Linux/MacOS users](https://github.com/ANTsX/ANTs/wiki/Compiling-ANTs-on-Linux-and-Mac-OS) and [Windows users](https://github.com/ANTsX/ANTs/wiki/Compiling-ANTs-on-Windows-10).

## <i class="fab fa-docker"></i> Local installation ("docker containers")

If you have a working Docker installation and would like to use the workshop's Docker image, you can run the following command in your terminal:

```bash

docker run --rm -p 9999:8888 -e JUPYTER_ENABLE_LAB=yes nipreps/nipreps-book:latest

```

This pulls the latest release of the nipreps/nipreps-book image from Docker Hub.
It then starts a container running a Jupyter Notebook server and exposes the server on host port 9999.
The server logs are printed to the terminal.
Visiting `http://127.0.0.1:9999/?token=<token>` in a browser loads JupyterLab, where token is the secret token printed in the terminal.
Docker destroys the container after notebook server exit.

```{tip}
If you'd like to add a folder on your computer to access within the container (for example, your own dMRI dataset), you can do so by adding the `-v <folderpath>:/home/jovyan/work` flag to the `docker run` command.
```
