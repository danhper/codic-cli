# Codic

Python CLI and library for [Codic](https://codic.jp/).

## Installation

```sh
pip install codic
```

## Usage

```
usage: codic [-h] [-t TOKEN]
             [-c {camel,pascal,lower-underscore,upper-underscore,hyphen}]
             [-f {text,json}]
             TEXT

get name from codic API

positional arguments:
  TEXT                  the text to translate

optional arguments:
  -h, --help            show this help message and exit
  -t TOKEN, --token TOKEN
                        Codic API token
  -c {camel,pascal,lower-underscore,upper-underscore,hyphen}, --casing {camel,pascal,lower-underscore,upper-underscore,hyphen}
                        Casing for the generated variable
  -f {text,json}, --format {text,json}
                        Choose the output format
```

The settings will be automatically saved in `~/.codicrc`, so you only need
to pass your API token the first time.

You can get an API token at https://codic.jp/my/api_status

### Example

```sh
$ codic --token MY_TOKEN 有効
有効: valid, enabled, active, available
$ codic 繰り返す
繰り返す: repeat, iterate
$ codic 英語難しい
難しい: difficult
英語: english
```
