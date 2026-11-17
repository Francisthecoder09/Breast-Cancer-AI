# Breast Cancer AI

An academic machine-learning project investigating feature selection and Support Vector Machines (SVMs) for breast cancer diagnosis. The planned study will use the Wisconsin Diagnostic Breast Cancer data and evaluate diagnostic errors, with particular attention to false negatives. This setup provides the Python environment and notebook outline; the full model has not yet been implemented.

## Technologies

Python, Jupyter Notebook, pandas, NumPy, Matplotlib, Seaborn, scikit-learn, SciPy, ucimlrepo, and joblib. VS Code's Python and Jupyter extensions are used to edit and run the notebook.

## Setup

Open this folder (`Breast-Cancer-AI`) in VS Code. The project-local `.venv` is selected in `.vscode/settings.json`, and the notebook is registered with the `Breast Cancer AI` kernel.

In PowerShell, activate the environment for the current terminal session:

```powershell
.\.venv\Scripts\Activate.ps1
```

If PowerShell blocks the activation script, do not change the machine or user execution policy. You can invoke the same environment directly instead:

```powershell
$env:PYYAML_FORCE_LIBYAML = "0"
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\jupyter.exe notebook
Remove-Item Env:PYYAML_FORCE_LIBYAML
```

Install dependencies with this PowerShell command sequence:

```powershell
$env:PYYAML_FORCE_LIBYAML = "0"
python -m pip install -r requirements.txt
Remove-Item Env:PYYAML_FORCE_LIBYAML
```

The environment variable tells PyYAML to skip its optional LibYAML C extension, avoiding a compiler requirement on Python versions without a matching PyYAML wheel. Jupyter uses PyYAML’s pure-Python implementation. If the environment is not activated, replace `python` with `.\.venv\Scripts\python.exe` in the install command.

## Open and run the notebook

1. Open the `Breast-Cancer-AI` folder in VS Code.
2. Open `notebooks/Breast_Cancer_Diagnosis_AI.ipynb`.
3. Select the `Breast Cancer AI` kernel if VS Code prompts for one.
4. Run the library import cell. The remaining sections are headings ready for project work.

The notebook kernel is registered for the current Windows user. To launch the classic Jupyter interface, activate the environment and run `jupyter notebook`, or run `.\.venv\Scripts\jupyter.exe notebook`.

## Run online with Jupyter and Binder

Windows Smart App Control on this computer blocks a compiled pandas library in the local virtual environment. Keep Smart App Control enabled and use a hosted Jupyter environment instead.

Binder can build a temporary JupyterLab environment from a public GitHub repository. The project repository must be public for the standard Binder service. Sessions are temporary, so download or save your notebook changes before the session ends.

After the project is published to GitHub:

1. Open [mybinder.org](https://mybinder.org/).
2. Enter the public GitHub repository URL and select **Launch**.
3. In Binder's JupyterLab file browser, open `notebooks/Breast_Cancer_Diagnosis_AI.ipynb`.
4. Select the **Breast Cancer AI** kernel if prompted, then run notebook cells with **Shift+Enter**.

The primary notebook contains the project outline and library imports only; the full model has not been implemented.

Do not commit `.venv`, private datasets, generated model files, or notebook checkpoints. These are excluded by `.gitignore`.

## Project folders

- `dataset/`: downloaded or prepared datasets (ignored by Git by default).
- `notebooks/`: exploratory and project notebooks.
- `src/`: reusable Python source code.
- `models/`: saved model artifacts (ignored by Git by default).
- `reports/`: written reports and analysis outputs.
- `reports/figures/`: generated figures (ignored by Git by default).
- `.venv/`: isolated Python environment; not tracked by Git.
- `.vscode/`: workspace settings that select this environment.
