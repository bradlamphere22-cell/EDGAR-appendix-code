# EDGAR-appendix-code

# 

This repository contains the \*\*appendix PDF\*\* and the \*\*reproducible Jupyter notebook code\*\* referenced in \*“A Random Walk Down EDGAR Street”\*.



> Note: The main article PDF is \*\*not\*\* included here.



---



\## Contents



\- `appendix/Appendix.pdf`  

&nbsp; The supplemental appendix referenced by the article.



\- `notebooks/A Random Walk Down EDGAR Street.ipynb`  

&nbsp; The reproduction notebook that generates the specific figures and tables referenced in the article.



\- `data/edgar\_concise\_sanitized.json`  

&nbsp; Sanitized input data used by the notebook.



\- `LICENSE`  

&nbsp; Custom license governing use and redistribution of the notebook and associated materials.



---



\## Quick start



\### Option A: pip (minimal)

1\. Create and activate a virtual environment (recommended).

2\. Install dependencies:

&nbsp;  ```bash

&nbsp;  pip install -r requirements.txt

Launch Jupyter:



bash

Copy code

jupyter notebook

Open and run:



notebooks/reproduce.ipynb

(Kernel → Restart \& Run All)



Option B: conda (if you prefer conda)

If you provide an environment.yml:



bash

Copy code

conda env create -f environment.yml

conda activate edgar-appendix-code

jupyter notebook

Reproducing figures and tables

The notebook is organized into independent sections. Each major section includes its own imports and file load, so a reader can review or run a single section without running the rest.



When run, the notebook writes outputs to:



figures/ — generated plots (publication-grade figures)



tables/ — generated tables / regression summaries (as applicable)



If these folders do not exist, the notebook will create them.



Notes on data

The notebook reads a sanitized JSON file:



data/edgar\_concise\_sanitized.json



If you relocate the JSON, update the IN\_JSON = ... assignment near the top of the relevant notebook section(s).



Provenance / “original notebook”

The file notebooks/reproduce.ipynb is the original reproduction notebook referenced by the redistribution conditions in LICENSE.

If you redistribute a modified version, please follow the requirements in LICENSE (including providing the unmodified original notebook alongside modified versions).



License

See LICENSE for the full terms.



Contact / Issues

If you find a reproduction problem (environment drift, dependency conflicts, or a path issue), please open a GitHub Issue with:



your OS + Python version



the command you used to install dependencies



the full error traceback

