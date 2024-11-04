[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/swKMSSMl)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=16850958&assignment_repo_type=AssignmentRepo)
# Computer Graphics Booting Up

## Let's start with ModernGL

This lab stands to prepare the moderngl development environment. Below the steps and requirements for initial coding tasks. Please make sure to edit the python provided files; for dependencies, you can add the files you need.

1. Install moderngl and its dependencies
2. Make sure that the following programs run
    - [`01_hello_world.py`](./01_hello_world.py)
    - [`06_multiple_objects.py`](./06_multiple_objects.py)
    - [`09_models_and_images.py`](./09_models_and_images.py)
        - _Modify this program to change the box's texture to a correctly aligned TEC logo_
3. Document how to execute the 3 programs in the section below.

* For documentation and missing dependencies, follow these links:
    - https://github.com/moderngl/moderngl
    - https://moderngl.readthedocs.io/

## How to run your program
# The file 'environmet.txt' includes a full config of conda for this project
#### 1\. Install Miniconda

If Miniconda is not already installed on your system:

`wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh`

Follow the on-screen instructions to complete the installation and initialize Conda.

#### 2\. Create a New Conda Environment

Create and activate a new Conda environment with Python 3.10:

`conda create -n myenv python=3.10
conda activate myenv`

#### 3\. Install Required Packages

1.  **Install `pygame`**:

    `conda install -c conda-forge pygame`
    or use 
    `pip install pygame`

2.  **Install `moderngl`** (for OpenGL context handling):

    `pip install moderngl`

3.  **Install `PyGLM`** (for GLM functionality):

    `pip install PyGLM`

4.  **Install `numpy`**:

    `pip install numpy`

5.  **Install `Pillow`** (for image handling):

    `pip install pillow`

6.  **Install `objloader`** (for handling 3D object files):

    `pip install objloader`

#### 4\. Adjust OpenGL Context Version in `pygame`

In your program, ensure the OpenGL context version and profile are set to 3.3 Core Profile. Insert these lines before the `pygame.display.set_mode()` call:

```
import pygame
# Set OpenGL context to version 3.3 core profile
pygame.display.gl_set_attribute(pygame.GL_CONTEXT_MAJOR_VERSION, 3)
pygame.display.gl_set_attribute(pygame.GL_CONTEXT_MINOR_VERSION, 3)
pygame.display.gl_set_attribute(pygame.GL_CONTEXT_PROFILE_MASK, pygame.GL_CONTEXT_PROFILE_CORE)
```

This ensures that the OpenGL context supports GLSL version 330 as specified in the shaders.

#### 5\. Running the Program

After setting up your environment and ensuring OpenGL context compatibility, run the included files. 

## Grading Policy

- 25% - `01_hello_world.py` is running with no errors
- 25% - `06_multiple_objects.py` is running with no errors
- 25% - `09_models_and_images.py` is running with the requested change (TEC logo texture)
- 25% - Documentation on how to run your programs