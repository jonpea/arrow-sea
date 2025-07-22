# ARROW SEA 2025 class 

Support material for a short course on Energy Pricing, presented at the 2025 edition of the [ARROW](https://arrowosw.org/) [Summer Education Accelerator](https://arrowosw.org/empower/summer-education-accelerator-sea/).

The session covered marginal priciong, DC optimal power flow (DC-OPF) via linear programming (LP), and security-constraiend unit commitment (SCUC) via mixed-binary linear programming (LP).

## Repository contents

Demonstration notebooks were hosted in [DeepNote](https://deepnote.com/) for the course, but can just as well be run locally on your PC.

| File                                               | Description                                                                                 | See also                                                    |
| -------------------------------------------------- | ------------------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| [slides.pdf](./slides.pdf)                         | Course slides                                                                               | Markdown source [slides.md](./slides.md)                    |
| [part1_mp.ipynb](./part1_mp.ipynb)                 | Reviews the graphical approach to marginal pricing at a single bus                          | Script version [part1_mp.py](./part1_mp.py)                 |
| [part2_opf.ipynb](./part2_opf.ipynb)               | Presents the LP formlution for DC-OPF on a general network, and visualizes the results      | Script version [part2_opf.py](./part2_opf.py)               |
| [part3_congestion.ipynb](./part3_congestion.ipynb) | Investigates congestion phenomena on a small three-node network, following Fu & Li (2006)   | Script version [part3_congestion.py](./part3_congestion.py) |
| [part4_uc.ipynb](./part4_uc.ipynb)                 | Presents the mixed-binary LP formulation of the SCUC problem and visualizes the results     | Script version [part4_uc.py](./part4_uc.py)                 |
| [requirements.txt](./requirements.txt)             | Python package requirements for local installation with `pip`                               |                                                             |
| [Dockerfile](./Dockerfile)                         | Container package requirements for remote installation in [DeepNote](https://deepnote.com/) |                                                             |

> ⚠️ The mixed-binary LP in [part4_uc.ipynb](./part4_uc.ipynb) takes some time to solve.

## Installation

> ⚠️ [PyGraphviz](https://pygraphviz.github.io/) requires system-installed [Graphviz](https://graphviz.org/) libraries. 
> Please install these before running `pip install`.

1. Install [Graphviz](https://graphviz.org/) and create a Python virtual environment:
   - On Ubuntu/Debian:
    ```bash
    sudo apt-get install graphviz libgraphviz-dev
    python -m venv .venv
    source .venv/bin/activate
    ```
   - On Mac:
    ```zsh
    brew install graphviz python
    python3 -m venv .venv
    source .venv/bin/activate
    ```
   - On Windows:
    ```powershell
    # For cmd.exe:
    .venv\Scripts\activate.bat

    # For PowerShell:
    .venv\Scripts\Activate.ps1
    ```

2. Install the Python dependencies in the active virtual environment:
   ```bash
   pip install -r requirements.txt
   ```

