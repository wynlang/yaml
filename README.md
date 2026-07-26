# yaml - Official Wyn Package

Simple YAML parser (key: value). Pure Wyn.

## Install

```bash
wyn pkg install github.com/wynlang/yaml
```

## Usage

```wyn
import yaml

var config = "host: localhost\nport: 6379\n# comment lines are skipped"

print(yaml.yaml_get(config, "host"))    // localhost
print(yaml.yaml_get(config, "port"))    // 6379
print(yaml.yaml_has(config, "host"))    // true
print(yaml.yaml_has(config, "missing")) // false
```

## API

| Function | Description |
|----------|-------------|
| `yaml_get(content, key)` | Value for `key`, or `""` if absent |
| `yaml_has(content, key)` | True if `key` is present |
| `yaml_parse(content)` | Parse into a HashMap (same-module use only — HashMap values cannot cross an import boundary) |
