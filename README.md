# DSCI-522-Group-17-Repository

## Python environment setup

### Prerequisites

Install Git, uv, and Quarto:

- Git: https://git-scm.com/downloads
- uv: https://docs.astral.sh/uv/getting-started/installation/
- Quarto: https://quarto.org/docs/get-started/

### Create the environment

Clone the repository and enter its folder:

```bash
git clone https://github.com/UBC-MDS-2026-27/DSCI-522-Group-17-Repository.git
cd DSCI-522-Group-17-Repository
```

Recreate the Python environment using the committed lockfile:

```bash
uv sync --locked
```

The project uses Python 3.12. uv creates a local `.venv` directory and installs the recorded dependencies.

### Verify the environment

Run:

```bash
uv run python -c "import pandas, sklearn, matplotlib, jupyter; print('All four packages imported successfully')"
```

Check that Quarto is installed:

```bash
quarto --version
```

Use `uv run` to run Python commands in the project environment; manual activation is not required.

### Render a Quarto report

From the repository root, use this command, replacing the example path with the actual report's path:

```bash
uv run quarto render analysis/your-report-name.qmd
```

The analysis report has not been added yet, so this example path is a placeholder.

### Environment verification status

The environment was tested on macOS using Python 3.12.14 and Quarto 1.10.18. A temporary Quarto document successfully imported the analysis packages, executed Python from the project's `.venv`, and rendered an HTML page containing a plot.

Windows verification and rendering of the final analysis report are pending.