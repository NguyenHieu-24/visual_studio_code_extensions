# Visual_Studio_Code_Extensions

[![Python Version](https://img.shields.io/badge/python-3.13%2B-blue)](https://www.python.org/)
[![Package Manager](https://img.shields.io/badge/uv-managed-purple)](https://github.com/astral-sh/uv)
[![Code Style](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

**vsc-extensions** is a Python-based project template designed for high-performance data processing and extension development. It leverages modern tooling and libraries to provide a robust environment for data-intensive tasks.

## 🚀 Key Features

* **Modern Package Management:** Built with `uv` for lightning-fast dependency resolution and environment management.
* **High-Performance Data Stack:**
    * **[Polars](https://pola.rs/):** Blazing fast DataFrames.
    * **[DuckDB](https://duckdb.org/):** In-process SQL OLAP database management system.
* **Ready-to-Use:** pre-configured for Python 3.13+.

## 🛠 Prerequisites

Before you begin, ensure you have the following installed:

* **uv** (An extremely fast Python package installer and resolver):
    ```bash
    # On macOS/Linux
    curl -LsSf [https://astral.sh/uv/install.sh](https://astral.sh/uv/install.sh) | sh

    # On Windows
    powershell -c "irm [https://astral.sh/uv/install.ps1](https://astral.sh/uv/install.ps1) | iex"
    ```

## 📦 Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/yourusername/vsc-extensions.git](https://github.com/yourusername/vsc-extensions.git)
    cd vsc-extensions
    ```

2.  **Initialize the environment and install dependencies:**
    This project uses `uv` to manage the lockfile and virtual environment automatically.
    ```bash
    uv sync
    ```
    *Note: This respects the configuration in `pyproject.toml` and `uv.lock`.*

## 💻 Usage

To run the main application entry point:

```bash
uv run main.py
