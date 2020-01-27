# FDL Lecture Notebooks

Repository containing lecture code notebooks.

## Remote Getting Started Guide

By default, clicking on the following image will open the notebooks up in 
Google Colab.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fdluiuc/lecture-notebooks/)

Then, select the appropriate notebook.

## Local Getting Started Guide

First, download and install [miniconda](https://docs.conda.io/en/latest/miniconda.html).

Once installed, make sure everything is up-to-date with:

```bash
conda update -n base -c defaults conda
```

Depending on your operating syste, you may need to do additional configurations.

In particular:

- **Windows**:  Use either [Windows PowerShell](https://docs.microsoft.com/en-us/powershell/)
   or [Windows Subsystems Linux 2.0](https://docs.microsoft.com/en-us/windows/wsl/wsl2-install)
- **macOS**: Install Xcode CLI developer tools by opening `Terminal`, found under
`Applications` -> `Utilities` -> `Terminal.app`, and typing:

```bash
sudo xcode-select --install
```

Having done this, please pick one of the course environments to use:

- **[uiuc_fdl_cpu.yaml](https://raw.githubusercontent.com/fdluiuc/lecture-notebooks/master/uiuc_fdl_cpu.yaml)** for CPU only-training (any platform); or
- **[uiuc_fdl_gpu.yaml](https://raw.githubusercontent.com/fdluiuc/lecture-notebooks/master/uiuc_fdl_gpu.yaml)** for GPU enabled training (requires Windows/Linux).


We encourage installing the course environment for CPU only-training as 
you will likely need to use cloud resources (
[Google Colab](https://colab.research.google.com/) or 
[HAL](https://wiki.ncsa.illinois.edu/display/ISL20/HAL+cluster)) to efficiently
train models. 

```bash
# Download
wget https://raw.githubusercontent.com/fdluiuc/lecture-notebooks/master/uiuc_fdl_cpu.yaml

# Create an environment called "uiuc_fdl_cpu" with packages installed.
conda env create -f uiuc_fdl_cpu.yaml
```

From there, make sure to activate the `uiuc_fdl_cpu` environment to use
the pre-setup environment when working on course items.

```bash
# Change from "base"/global into course environment
conda activate uiuc_fdl_cpu

# Return to "base"/global environment
conda deactivate
```

Please **avoid** installing any packages globally.

Lastly, clone the repository to your personal computer using:

```bash
git clone git@github.com:fdluiuc/lecture-notebooks.git fdl-lecture-notebooks
```

Grab new notebooks using:

```bash
git pull
```

To view or modify a notebook locally, use:

```
# Change to where lecture notebooks repository
# is stored on your computer.
cd path/to/lecture-notebooks

# Launch jupyter to view notebook
jupyter notebook
```

