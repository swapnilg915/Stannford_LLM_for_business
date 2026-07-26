# Stanford TECH16 LLM Notebooks

This folder contains Stanford TECH16 notebooks for Large Language Model homework and projects. The notebooks are prepared for Python 3.10 and read secrets from environment variables.

## Included Notebooks

- `Insurance_Claim_settlement_System.ipynb`
- `Insurance_Claim_settlement_System(1).ipynb`
- `TECH16_LLM_WEEK_1_HW.ipynb`
- `TECH16_LLM_Week_3_HW.ipynb`
- `TECH16_WEEK_2_HW.ipynb`
- `TECH16_Week_6_HW.ipynb`
- `Stanford_Notebook_Scaffold.ipynb`

## Python 3.10 Compatibility

These notebooks have been cleaned and validated for Python 3.10 metadata, syntax, dependency resolution, and output-free notebook state. The dependencies are pinned in `requirements.txt`.

## Setup (Local)

1. Create a Python 3.10 virtual environment.

```bash
python3.10 -m venv .venv
source .venv/bin/activate
```

2. Install dependencies.

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

3. Set your OpenAI API key.

```bash
read -s OPENAI_API_KEY
export OPENAI_API_KEY
```

4. Run a notebook with Jupyter or VS Code.

```bash
jupyter notebook
```

### Execute a notebook from the command line

```bash
jupyter nbconvert --to notebook --execute Insurance_Claim_settlement_System.ipynb --output executed.ipynb
```

## Setup on Google Colab

1. Upload the notebook to Colab.
2. Install dependencies from `requirements.txt`.
3. Store `OPENAI_API_KEY` in Colab secrets or another environment-variable manager.

## Notes

- The notebooks have been sanitized to remove hard-coded keys.
- Store API keys securely and do not commit them.
- Gradio launch cells are opt-in. Set `LAUNCH_GRADIO=true` before running them.
- Week 6 skips the local Mistral model by default because it is large. Set `RUN_LOCAL_MODEL=true` to download and run it.
- The insurance claim notebooks use `India_motor_vehicle_act_1988.pdf` when present, otherwise they create a small sample rules file for runnable demos.
- The `requirements.txt` file includes packages required to run the Stanford notebooks on Python 3.10.

## Validation status

- Python 3.10.14 dependency dry-run completed successfully.
- All notebooks are valid nbformat v4 and use Python 3.10 kernel metadata.
- All notebook outputs and execution counts were cleared.
- A Python syntax validation pass was completed for all code cells.
