# Open-Protac-INVENT

Source code for our paper "---". This adaptation is built on top of Protac-invent (https://github.com/jidushanbojue/Protac-invent), which itself is based on REINVENT, reinvent-scoring, and DockStream. 


This adaptation also integrates Roshambo (https://github.com/molecularinformatics/roshambo) to enable shape-based scoring functionality. We thank the original authors of all these projects for sharing their work.


## Description
Open-Protac-INVENT is an open-source adaptation of Protac-Invent, designed for PROTAC linker generation using reinforcement learning and docking-based scoring. 
The original Protac-Invent framework combines **generative modeling from REINVENT** with **scoring functions from reinvent-scoring** and **docking workflows from DockStream** to enable reinforcement learning-driven linker design.

In this adaptation, we replace proprietary shape-similarity components (e.g., ROCS, Omega) with fully **open-source alternatives** using Roshambo and RDKit for 2D-to-3D conformer generation, shape-based scoring, and energy minimization. These modifications make the workflow more accessible and reproducible, allowing it to be used without commercial licenses.

The repository includes:

- Updated pipelines for open-source shape similarity scoring (**Roshambo + RDKit**).  
- Integration with **DockStream** for docking and post-docking analysis.  
- Configurable **JSON templates** for custom linker generation tasks.  
- Example datasets and results to help users reproduce the workflow.


## Diagrams
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

### 3. Open terminal, navigate to the cloned repository, and create the Conda environment
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



## Usage
### 1. Edit the Template JSON
- Locate the template JSON file (for example: results/LINK_invent/BTK/template.json).
- Modify the **file and folder paths** in the template as needed.
- Other parameters can remain unchanged for a standard run.

### 2. Run the Model
Execute the following command to start the run using the edited JSON:
```bash
$ python input.py template.json
```



## License & Attribution

This project is licensed under the **Apache License 2.0**, except where otherwise noted.

Portions of the code, specifically under `src/roshambo/`, are derived from [Roshambo](https://github.com/molecularinformatics/roshambo) and are licensed under the **GNU General Public License v3.0 (GPL-3.0)**.  
Modifications were made to integrate Roshambo into this project. Users must comply with both licenses where applicable.

Full license details can be found in the [LICENSE](./LICENSE) file.  
For the GPL-3.0 portion, see [src/roshambo/LICENSE](./src/roshambo/LICENSE).

We also acknowledge upstream work:
- [Protac-Invent](https://github.com/jidushanbojue/Protac-invent)
- [reinvent-scoring](https://github.com/MolecularAI/reinvent-scoring)
- [DockStream](https://github.com/MolecularAI/DockStream)
- [REINVENT](https://github.com/MolecularAI/Reinvent)
