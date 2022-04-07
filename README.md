# Colour Quantisation

![Python >= 3.10.2](https://img.shields.io/badge/python-%3E%3D%203.10.2-blue?style=flat-square) ![Testing TBD%](https://img.shields.io/badge/coverage-TBD%25-red?style=flat-square)

## Installation

I have chosen to use `poetry` and `pyenv`. To setup and use the environment:

```shell
poetry install
poetry shell
```

This will automatically create a virtual environment and install the required dependencies.

## Usage

Inputs:
- filename of a single image file to quantise OR a directory of images to quantise
- filename with a list of allowed colours (R,G,B or RRGGBB hex)
- [optional] an output directory name to save the quantised image to
    if omitted, will display the quantised image without saving it
- [optional] dithering type (NONE, ???, ???)
    if omitted, will default to ???

```shell
python -m colquant "./input.png" --colours="./colours.txt" --output_dir="./output/" --dithering="NONE"
```

## Development

### Pre-commit Checks

To run them manually:

```shell
pre-commit run --all-files
```

This will run a series of linting and type-checking (`flake8`, `black`, `mypy`) and tell you what needs to be fixed. You may need to run it more than once. It will be automatically run when attempting to commit a change.

### Testing

To run tests:

```shell
pytest
```

For test coverage:

```shell
pytest --cov=pitch tests/
```
