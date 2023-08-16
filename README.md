# SCE_SDTM_TEMPLATE

This repo and corresponding Domino Project contains the folder structure to template a study wide SDTM project.

This repo project is copied by Data Management to instantiate a new study specfic SDTM GitHub repo and Domino Project.

# Directory structure

The programming is created in a typical clinical trial folder structure, where the production (prod) and qc programs have independent directory trees.

Reporting effort level standard code (e.g. SAS macros) should be stored in the `share/macros` folder.

The global `domino.sas` autoexec progam is also included in the repository to appropriately set up the SAS environment. 

```
repo
│   domino.sas
├───prod
│   └───sdtm
├───qc
│   └───sdtm
└───utilities
        init_datasets.py
└───share
    └───macros
```

# Setup

1. Create a new project, named `CDISC01_SDTM_YOURNAME`, from copying this project. This will create a new project and a new study specfic GitHub repo.
1. Run `utilities/dataset_init.py` as a job to create the appropriate SDTM Domino Datasets (SDTMBLIND, SDTMUNBLIND and METADATA).

# Naming convention

The programs follow a typical clinical trial naming convention, where the SDTM programs are named after the datasets they are producing (e.g. DM.sas, AE.sas, etc...)

# Support

Programming was created by Veramed Ltd. on behalf of Domino Data Lab, Inc.
