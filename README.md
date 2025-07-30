# Open-Protac-INVENT
Source code for our paper "---". This adaptation is built on top of Protac-invent (https://github.com/jidushanbojue/Protac-invent), which itself is based on REINVENT (https://github.com/MolecularAI/Reinvent) and DockStream (https://github.com/MolecularAI/DockStream). 


This adaptation also integrates Roshambo (https://github.com/molecularinformatics/roshambo) to enable shape-based scoring functionality. We thank the original authors of all these projects for sharing their work.


![Architecture Overview](docs/architecture.jpg)
*Figure 1: Initial Integration Diagram (To be updated)*





![General Workflow](docs/general_workflow.jpeg)  
*Figure 2: General workflow of Open-Protac-INVENT. Adapted from [Protac-invent](https://github.com/jidushanbojue/Protac-invent) under [Apache 2.0 License](https://www.apache.org/licenses/LICENSE-2.0).*


## Installation

### 1. Prerequisites
- Install [Conda](https://docs.conda.io/en/latest/miniconda.html) 
- Ensure `git` is installed and available in your PATH.

### 2. Clone This Repository
```bash
$ git clone https://github.com/SaiCharithReddy/Open-Protac-INVENT.git
$ cd Open-Protac-INVENT
```

### 3. Open a terminal/shell, navigate to the cloned repository, and create the Conda environment
```bash
$ conda env create -f environment.yml
```

### 4. Activate the Environment
```bash
$ conda activate open-protac-invent
```

### 5. Install This Repo
```bash
$ pip install -e .
```
