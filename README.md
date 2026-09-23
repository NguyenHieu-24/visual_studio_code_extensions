<h1 align="center">Visual Studio Code Extensions</h1>
<p align="center">
  A minimal Python starter project with uv, Polars, and DuckDB.
</p>
<p align="center">
  <img src="https://img.shields.io/badge/Python-3.13%2B-3776AB?style=flat-square" alt="Python: 3.13 or later">
  <img src="https://img.shields.io/badge/Environment-uv-6E56CF?style=flat-square" alt="Environment: uv">
  <img src="https://img.shields.io/badge/Data-Polars-FFCD00?style=flat-square" alt="Data: Polars">
  <img src="https://img.shields.io/badge/SQL-DuckDB-FFF000?style=flat-square" alt="SQL: DuckDB">
</p>
<p align="center">
  <a href="#overview">Overview</a> ·
  <a href="#quick-start">Quick Start</a> ·
  <a href="#project-structure">Project Structure</a> ·
  <a href="#current-status">Current Status</a>
</p>

---

## Overview
`vsc-extensions` is a small Python project scaffold. It declares Polars and DuckDB as dependencies, pins Python 3.13 in `.python-version`, and provides a `uv.lock` file for reproducible dependency resolution. The current program prints a greeting; it does not yet use either data library.
> **Project status:** Despite the repository name, this archive does not contain a VS Code extension manifest, extension commands, or editor integration. It is a Python starter project that can be opened and developed in VS Code.

## At a Glance
| Component | Included in the repository | Current use |
|---|---|---|
| Python | `main.py`, Python 3.13+ requirement | Prints `Hello from vsc-extensions!` |
| uv | `uv.lock`, `.python-version` | Manages the project environment and dependencies |
| Polars | Declared in `pyproject.toml` | Available for future DataFrame processing |
| DuckDB | Declared in `pyproject.toml` | Available for future analytical SQL work |
| VS Code extension | No extension source or manifest | Not implemented |

---

## Quick Start
### 1. Install the prerequisites
Install [uv](https://docs.astral.sh/uv/getting-started/installation/) and use Python 3.13 or later. From the extracted project directory, you can ask uv to install the version selected by `.python-version`:
```sh
uv python install 3.13
```

### 2. Create the environment
```sh
uv sync
```

This creates a local `.venv` and installs dependencies from the project configuration and lockfile.

### 3. Run the program
```sh
uv run python main.py
```

Expected output:
```text
Hello from vsc-extensions!
```

<details>
<summary><strong>Working in Visual Studio Code</strong></summary>
<ol>
<li>Open the extracted repository folder in VS Code.</li>
<li>Run <code>`uv sync`</code> in the integrated terminal.</li>
<li>Select the Python interpreter from <code>`.venv`</code> if VS Code does not detect it automatically.</li>
<li>Run <code>`uv run python main.py`</code> in the integrated terminal.</li>

On Windows, the interpreter is under `.venv\Scripts\python.exe`; on macOS and Linux, it is under `.venv/bin/python`.
</ol>
</details>

<details>
<summary><strong>About setup.sh and Python versions</strong></summary>

`setup.sh` contains only `uv python install 3.15`. The project itself specifies Python **3.13** in `.python-version` and **3.13 or later** in `pyproject.toml`. For the documented setup, use `uv python install 3.13` followed by `uv sync`. The script neither syncs dependencies nor starts the application.

</details>

---

## Project Structure
| Path | Purpose |
|---|---|
| `main.py` | Small runnable entry point |
| `pyproject.toml` | Project metadata, Python requirement, and dependencies |
| `uv.lock` | Resolved dependency versions |
| `.python-version` | Preferred Python version: `3.13` |
| `setup.sh` | One-command attempt to install Python 3.15 through uv |
| `.gitignore` | Excludes virtual environments, caches, and build outputs |

## Current Status
The repository is ready as an environment for experiments, but it does not yet implement an extension or a data workflow. Its only runtime behavior is the greeting in `main.py`. There are no tests, dataset samples, extension package files, or usage examples for Polars and DuckDB in the supplied source.

## Roadmap
- Define whether the project will become a VS Code extension or a Python data application.
- Add a first runnable Polars and DuckDB example, with sample input and expected output.
- Align `setup.sh` with the Python version selected in `.python-version` and add dependency sync if the script remains necessary.
- Add focused tests and instructions for the resulting functionality.

## Contributing
Open an issue to describe the intended feature or submit a focused pull request. Include the command you ran and the output you observed. Keep dependency changes reflected in `pyproject.toml` and `uv.lock`.

## License
No license file is included in the supplied archive. Ask the project owner for permission before redistributing the code.

---

<p align="center"><a href="#vs-code-extensions">Back to top ↑</a></p>
