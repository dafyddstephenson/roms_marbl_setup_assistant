# roms_marbl_setup_assistant
NOTE: This repository was formally known as C-Star, which has [continued development as a python package](https://github.com/CWorthy-ocean/C-Star). This repo is now being maintained independently of C-Star.

## Overview
This code allows a user on a supported system to automate the process of configuring their environment and then obtaining and installing [ROMS](https://github.com/CESR-lab/ucla-roms) and [MARBL](https://github.com/MARBL-ecosys/MARBL).

Following a clean install of ROMS-MARBL, the setup assistant will prompt the user to install the [`roms_marbl_example`](https://github.com/CWorthy-ocean/cstar_blueprint_roms_marbl_example/tree/no_cstar) configuration, which is effectively a miniaturised version of a full-scale ROMS-MARBL simulation setup that can be run on a laptop, allowing the user to become familiar with using ROMS-MARBL.

## Setup
- Clone this repository and run (from the command line) the script `setup_roms_marbl` in the top-level directory, providing your system as an argument (e.g. `./setup_roms_marbl osx_arm64_gnu`). For a list of supported systems, run `setup_roms_marbl --help`.
- The setup script will obtain and compile any external code, and also make an environment on your machine to use when running ROMS-MARBL in future. To activate this environment, run the command `roms_marbl_env` after completing the setup (note you will have to restart your shell).
- Lastly, the setup script will ask if you would like to install and compile the [`roms_marbl_example`](https://github.com/CWorthy-ocean/cstar_blueprint_roms_marbl_example/tree/no_cstar) configuration, which will be compiled in the `cases` directory at the top level of this repository. If you choose to install, you can run the example case using `cases/roms_marbl_example/start_run.sh`
