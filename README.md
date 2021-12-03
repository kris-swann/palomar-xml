# Palomar XML

Simple CLI Tool to convert XLSX files to XML format following State provided specifications

### Requirements

* Python 3.9 or greater (python.org)

### Setup

If you need to use multiple versions of python for different projects (e.g. 2.7, 3.5, 3.8) use https://github.com/pyenv/pyenv (if on windows, see the Windows section of the Readme).

It is highly, highly recommended to use venv to prevent issues with system-wide installed packages

```
cd /path/to/palomar-xml
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
chmod +x ./convert.py
```

### Running

```
source .venv/bin/activate  # Can skip this if venv is already activated

# Call command with the format of the following
./convert.py <path to xlsx file> <worksheet name> <year> <quarter>

# Example (if *.xlsx file is in the palomar-xml directory)
./convert.py FL_2020_Q4.xlsx "2020 Q4 for xml" 2020 4
```

File will be output as `FSLSO_{Year}_{Quarter}.xml` in the `palomar-xml` directory

Do not forget that if any of the arguments contain spaces, you must wrap that argument in quotes. If problem persists, just remove spaces from file name and worksheet names and run command without any quotes.

If you forget any of this, run any of the following to get a short prompt of how to run

```
./convert.py
./convert.py help
./convert.py -h
./convert.py --help
```
