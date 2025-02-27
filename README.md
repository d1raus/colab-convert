# colab-convert

Atom/Hydrogen or VSCode/Python allows creating a python files split into cells with `# %%` separators with the ability to run cells via backend Jupyter session and interactively show results back.

More examples: [Jupyter Python VSCode examples](https://github.com/DonJayamanne/pythonVSCode/wiki/Jupyter-Examples), [Atom/Hydrogen Getting Started](https://nteract.gitbooks.io/hydrogen/docs/Usage/GettingStarted.html).

[colab-convert](https://pypi.python.org/pypi/colab-convert) python module converts files: .ipynb to .py and .py to .ipynb.

**colab-convert** is a fork of the [ipynb-py-convert](https://github.com/kiwi0fruit/ipynb-py-convert).


## Install

```bash
conda install -c defaults -c conda-forge colab-convert
```
or
```bash
pip install colab-convert
```


## Troubleshooting

* If encoding problems on Windows try using `python>=3.7`, setting `set PYTHONUTF8=1` in Windows console and use `colab-convert` for UTF-8 files only. If using [Git-Bash on Windows](https://git-scm.com/download/win) setting:

```bash
export LANG=C.UTF-8
export PYTHONIOENCODING=utf-8
export PYTHONUTF8=1
```
should be enough. Also try setting default Bash settings to UTF-8: [Options] - [Text] - [Locale / Character set] - [C / UTF-8]. It might affect all Bash runs so there would be no need to setting encoding every time. 


## Example

`colab-convert examples/plot.py examples/plot.ipynb`

or

`colab-convert examples/plot.ipynb examples/plot.py`


**VSCode**

![](https://github.com/MSFTserver/colab-convert/raw/master/examples/vscode.png)

Markdown cells are converted to python multiline strings `'''`. Code cells are left as is. `# %%` is used by vscode as the cell marker on which 'Run Cell' action is available.

Metadata is converted from notebooks into .py and vise versa using `# !!` to denote the meta data lines in the .py files


**Jupyter ipynb notebook**

![](https://github.com/MSFTserver/colab-convert/raw/master/examples/jupyter.png)
