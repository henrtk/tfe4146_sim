# TFE 4146 sim

This project builds on the python package [Sesame](https://sesame.readthedocs.io/en/latest/index.html#) and contains examples for numerical simulations of p-n junctions. The examples are developed as support material to the course TFE 4146 Semiconductor Devices at NTNU, mostly developed by Fredrik Feyling (@fredief). This requires at least Python 3.4 or above.

For simplicity, only the required part of the sesame source code is copied into the repository, such that no installation of sesame is required. Please refer to the [Sesame](https://sesame.readthedocs.io/en/latest/index.html#) documentation for a detailed description of the simulation back-end.

## Installation
Open a terminal window and navigate into a directory where you want to run the python simulations, e.g.:
```bash
    cd /path/to/your/work/directory
```

Clone this repository,
using the web url:
```bash
    git clone https://github.com/henrtk/tfe4146_sim.git
```
or with ssh:
```bash
    git clone git@github.com:henrtk/tfe4146_sim.git
```

To make sure that the simulation's package dependencies' installation is clean and without incompabilities with respect to your global Python installation (that means, the one you usually get when you type python or pip into the terminal), we will opt for a *virtual environment*. This instantiates a python version which is only active in this project. *Note* This has only been tested to work for Python 3.10 to 3.12, please consider making sure that the python installation which is called when you enter the command `python` has the correct version. If you have multiple Python installations in your system, you may try calling for example `python3.12` or `path/to/your/pythoninstallation/python.exe` instead of `python`.

To create a virtual environment, enter the following into terminal:

```bash
    cd .\\tfe4146_sim # move/change directory (cd) into the installed project folder
    python -m venv tfe4146_venv # creates a virtual environment for this project with name tfe4146_venv
    # using Windows, run the following command:
    tfe4146_venv\\Scripts\\activate 
    # using MacOS/Linux:
    source tfe4146_venv/bin/activate
```

The terminal (atleast when using WindowsPowerShell) will now be marked with (tfe4146_venv), indicating that you're working within the virtual environment. The virtual environment has its own separate Python installation. To deactivate it, enter the command `deactivate`.

You may now install the required packages to the local Python version using

```bash
    pip install -r requirements.txt
```

> **_NOTE:_** If there is trouble installing pandas and/or kiwisolver (ignore this otherwise) in the requirements, first try to install Microsoft Visual Studio Build Tools as prompted in the error message using https://visualstudio.microsoft.com/visual-cpp-build-tools/. You may have to restart your computer for the changes to take effect. If this also fails, go into requirements.txt and delete the pandas and kiwisolver entries, save the changes, and try the above command again. Experience shows that the simulation *will work* without these, but, the interactive plotting in Jupyter may give (non-significant, but annoying) errors which are possible to ignore. 


Jupyter is automatically installed as a dependency of the required packages. Run the following command from your activated virtual environment to open a Jupyter server using the local Python version by entering
```bash
    jupyter-notebook
```
into the terminal, which should open up your browser in Jupyter, where you may move to `/notebooks/pn_junction`.ipynb to start working! 


If you prefer to use Jupyter notebooks outside of a browser, like VSCode, you may do so by selecting the virtual environment's python installation, `.\tfe4146_venv\Scripts\python.exe`, as the notebook's kernel. To view it as a kernel option in the VSCode extension for Jupyter, you need to open the `.\tfe4146_sim\`-folder in VSCode. When doing so, the local Python version will show up as the recommended Jupyter kernel. Select it as the kernel for the notebook.

## Usage

See the comments in the examples and especially Problem set 4 on Blackboard.

