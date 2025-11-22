# lang-graph

Simple instructions to set up a Python virtual environment and run the Jupyter notebooks in this repository.

## Prerequisites
- Python 3.8 or newer installed
- Git (optional, to clone the repo)
- A terminal (macOS/Linux) or PowerShell / Command Prompt (Windows)

## Quick setup (macOS / Linux)
1. Clone the repository (if needed):
    git clone <repo-url>
    cd lang-graph

2. Create and activate a virtual environment:
    python3 -m venv .venv
    source .venv/bin/activate

3. Upgrade pip and install dependencies:
    pip install --upgrade pip
    pip install -r requirements.txt

    If there is no `requirements.txt`, install Jupyter and common packages:
    pip install jupyterlab ipykernel numpy pandas matplotlib networkx

4. (Optional) Register the virtual environment as a Jupyter kernel:
    python -m ipykernel install --user --name lang-graph --display-name "Python (lang-graph)"

5. Start Jupyter Lab / Notebook:
    jupyter lab
    # or
    jupyter notebook

6. Open the `.ipynb` files in the browser and select the "Python (lang-graph)" kernel if you registered it.

## Quick setup (Windows PowerShell)
1. Clone and change directory:
    git clone <repo-url>
    cd lang-graph

2. Create and activate venv:
    python -m venv .venv
    .\.venv\Scripts\Activate.ps1   # or Activate.bat in cmd.exe

3. Install dependencies:
    pip install --upgrade pip
    pip install -r requirements.txt

4. Register kernel (optional):
    python -m ipykernel install --user --name lang-graph --display-name "Python (lang-graph)"

5. Launch Jupyter:
    jupyter lab
    # or
    jupyter notebook

## Running notebooks in VS Code
- Open the repository folder in VS Code.
- Install the Python extension if you haven't.
- Select the virtual environment interpreter (bottom-right) or choose the "Python (lang-graph)" kernel in the notebook UI.
- Open and run the `.ipynb` files.

## Deactivate the virtual environment
- macOS / Linux / Windows (cmd/powershell):
  deactivate

## Troubleshooting
- "Module not found" errors: ensure you installed the required packages (`pip install -r requirements.txt`) and picked the correct kernel.
- Permission issues: try running installation commands without sudo; use virtual environments to avoid system-wide installs.
- If notebooks rely on specific versions, check for an `environment.yml` or pinned `requirements.txt` in the repo and use those.

## Notes
- Add a `requirements.txt` file to the repo for reproducible installs:
  pip freeze > requirements.txt
- For reproducible environments across machines consider adding an `environment.yml` (Conda) or specifying pinned package versions.
