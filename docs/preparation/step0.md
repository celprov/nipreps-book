# Before we start: How to follow this tutorial
This tutorial contains a mix of lecture-based and interactive components.
The interactive components can be executed in your personal computer locally or using the Binder service.
You are welcome to follow along however you like, whether you just want to listen or code along with us.
Each of the chapters involving code are actually Jupyter notebooks!

## Using Binder
Clicking the Binder icon in the top right corner will launch an interactive computing environment with all of the necessary software packages pre-installed.

```{figure} images/binder_link.png
:name: binder_link

Binder Link
```

## Local installation ("bare-metal")
If you would like to follow along using your own setup and you have a functional Python environment, you can:

```bash

# 1. clone this repository
git clone https://github.com/nipreps/nipreps-book

# 2. install the necessary python packages in your Python environment
cd nipreps-book && pip install -r requirements.txt

# 3. launch a Jupyter lab instance
jupyter lab

```

## Local installation ("docker containers")
