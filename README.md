# UV -  Python Package Manager

UV is a package manager and project management tool for Python, designed to solve long-standing dependency and project management issues that have historically been considered Python's weak points.

## Installation

### Mac/Linux
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

### Windows
```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

## What is UV?

UV is a Python project management tool inspired by Rust's Cargo, offering a unified interface for various tasks such as project initialization, dependency management, test execution, and script running. It emerged from a collaboration between the Rai project (created by Flask's creator Armin Ronacher) and Astral, the company behind Ruff.

## Key Features

- **Fast Dependency Resolution**: Advanced algorithms for quick and efficient dependency management
- **Project Management**: Simplified project initialization and management
- **Virtual Environment Handling**: Easy creation and management of virtual environments
- **Package Installation**: Streamlined package installation process
- **Workspace Support**: Handles complex projects with multiple repositories
- **Script Execution**: Run Python scripts with inline declared dependencies

## Main Commands

- `uv init`: Initialize a new Python project
- `uvx`: Execute Python programs without installation using temporary virtual environments
- `uv tool install`: Install tools within the UV environment
- `uv run`: Execute commands in the UV environment
- `uv python install`: Install specific Python versions
- `uv venv`: Create virtual environments
- `uv pip`: Interact with PIP for dependency management

## Quick Start

### 1. Create and Activate Virtual Environment
```bash
# Create virtual environment
uv venv

# Activate virtual environment (Mac/Linux)
source .venv/bin/activate
```

### 2. Managing Dependencies

#### Option 1: Using pyproject.toml directly
```bash
# Install dependencies from pyproject.toml
uv pip install -r pyproject.toml
```

#### Option 2: Using requirements.txt
```bash
# Generate requirements.txt from pyproject.toml
uv pip compile pyproject.toml -o requirements.txt

# Install dependencies from requirements.txt
uv pip install -r requirements.txt
```

### 3. Adding New Dependencies

UV provides a simple way to add new packages to your project. For example, to add pandas:

```bash
# Add pandas to your project (exemplary usage)
uv pip install pandas

# If you want to add it to your pyproject.toml with a specific version
uv add pandas==2.2.0
```

Your `pyproject.toml` will be updated with something like:

```toml
[project]
dependencies = [
    "pandas==2.2.0"
]
```

## Configuration

UV uses `pyproject.toml` for dependency management, providing a modern and standardized approach to Python project configuration.

## Advantages

- Standardized project management
- Improved dependency resolution
- Significantly faster package installation
- Single tool for multiple Python project management tasks
- Modern approach to Python development workflows

## Installation

UV can be installed through various methods:
- Shell command
- PIP
- System package managers

For specific installation instructions, please refer to the official UV documentation.

---

UV represents a significant step forward in Python's ecosystem, addressing the language's historical package and project management challenges with a modern, unified solution.
