![bash_unit CI](https://github.com/pforret/shini/workflows/bash_unit%20CI/badge.svg)
![Shellcheck CI](https://github.com/pforret/shini/workflows/Shellcheck%20CI/badge.svg)
![GH Language](https://img.shields.io/github/languages/top/pforret/shini)
![GH stars](https://img.shields.io/github/stars/pforret/shini)
![GH tag](https://img.shields.io/github/v/tag/pforret/shini)
![GH License](https://img.shields.io/github/license/pforret/shini)
[![basher install](https://img.shields.io/badge/basher-install-white?logo=gnu-bash&style=flat)](https://basher.gitparade.com/package/)

# shini

![shini](assets/unsplash.ini.jpg)

![Under Development](https://img.shields.io/badge/under-development-orange)

Bash .ini config file parser

## 🔥 Usage

```bash
Program: shini 0.0.4 by peter@forret.com
Updated: Aug  8 20:18:27 2021
Description: Bash .ini parser
Usage: shini [-h] [-q] [-v] [-f] [-l <log_dir>] [-t <tmp_dir>] [-d <default>] <action> <input?> <chapter?> <key?>
Flags, options and parameters:
    -h|--help        : [flag] show usage [default: off]
    -q|--quiet       : [flag] no output [default: off]
    -v|--verbose     : [flag] output more [default: off]
    -f|--force       : [flag] do not ask for confirmation (always yes) [default: off]
    -l|--log_dir <?> : [option] folder for log files   [default: /Users/pforret/log/shini]
    -t|--tmp_dir <?> : [option] folder for temp files  [default: /tmp/shini]
    -d|--default <?> : [option] name of chapter with default values  [default: _default]
    <action>         : [parameter] action to perform: chapters/setall/listall/get
    <input>          : [parameter] input file (optional)
    <chapter>        : [parameter] chapter name (optional)
    <key>            : [parameter] key name (optional)
                                  @github.com:pforret/shini.git                                             
### TIPS & EXAMPLES
# use `shini chapters` to list all chapters of a .ini file, e.g. to use in a loop
shini chapters production.ini | while read -r chapter ; do (...) done

# use shini setall to set all values of a chapter
shini setall production.ini frontend # and now all the variables in .ini have been set

# use shini listall to list all values of a chapter
shini listall production.ini frontend
# key1=value1
# key2=value2

# use shini get to get the value of 1 key for a certain chapter
port=$(shini get production.ini frontend http_port)

# you can add a chapter with default values
[_default]
http_port=80

# use shini check to check if this script is ready to execute and what values the options/flags are
shini check

# use shini env to generate an example .env file
shini env > .env

# use shini update to update to the latest version
shini check
```

## ⚡️ Examples

```bash
> shini .
# start PhpStorm with current folder as project
```

## 🚀 Installation

with [basher](https://github.com/basherpm/basher)

	$ basher install pforret/shini

or with `git`

	$ git clone https://github.com/pforret/shini.git
	$ cd shini

## 📝 Acknowledgements

* script created with [bashew](https://github.com/pforret/bashew)

&copy; 2021 Peter Forret
