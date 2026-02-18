# yaml — Official Wyn Package

Simple YAML parser (key: value). Pure Wyn.

## Install

```bash
wyn pkg install github.com/wynlang/yaml
```

## Usage

```wyn
var config = yaml_parse(File.read("config.yml"))
var host = config.get("host")
```
