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

To make sure that the simulation's package dependencies' installation is clean and without incompabilities with respect to your global Python installation (that means, the one you usually get when you type python or pip into the terminal), we will opt for a *virtual environment*. This instantiates a python version which is only active in this project. To do so, enter the following into terminal:

```bash
cd .\\tfe4146_sim # move/change directory (cd) into the installed project folder
python -m venv tfe4146_venv # creates a virtual environment for this project, with name tfe4146_venv
# using Windows:
.\\tfe4146\\Scripts\\activate 
# using MacOS/Linux
$ source tfe4146/bin/activate
```

The terminal (atleast when using WindowsPowerShell) will now be marked with (tfe4146_venv), indicating that you're using the virtual environment. To deactivate it, just enter the command `deactivate`.

You may now install the required dependencies

```bash
    pip install -r requirements.txt
```

Jupyter is installed by the required packages. Run the following command from you activated virtual environment to open a Jupyter server by using
```bash
jupyter-notebook
```
which should open up your browser in Jupyter, where you may move to `/notebooks/pn_junction`.ipynb to start working! 


If you prefer to use Jupyter notebooks outside of a browser, like VSCode, you may do so by selecting the virtual environment's python installation, `.\tfe4146_venv\Scripts\python.exe`, as the notebook's kernel. To view it as the recommended kernel option in the VSCode extension for Jupyter, you need to open the `.\tfe4146_sim\`-folder in VSCode, and then select it as the kernel for the notebook.

## Usage

See the comments in the examples and especially Problem set 4 on Blackboard.

