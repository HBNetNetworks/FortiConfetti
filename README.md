# FortiConfetti

**FortiConfetti: break down your FortiGate config into JSON bits.**

FortiConfetti is a simple Python tool that parses FortiGate configuration backup files (in their raw FortiOS format) and outputs structured JSON, making it easier to analyze, manipulate, or integrate FortiGate configurations into automation workflows.

## Features

- Converts FortiOS-style `.conf` backup files into structured JSON
- Lightweight and dependency-free (or minimal dependencies)
- Easily scriptable for batch conversion or integration
- Output structure designed to mirror the logical config hierarchy

## Example

```bash
$ forticonfetti ./backup.conf > config.json
```

## Installation

(Coming soon via PyPI)

```bash
pip install forticonfetti
```

## Usage

You can run the parser as a standalone CLI tool or import it as a module in your Python scripts:

### CLI

```bash
forticonfetti path/to/config.conf
```

### Python

```python
from forticonfetti import parse_config

with open("backup.conf") as f:
    config_data = parse_config(f.read())

print(config_data)
```

## Roadmap

- [ ] CLI argument support (`--pretty`, `--output`, etc.)
- [ ] Error handling for malformed or partial config files
- [ ] JSON schema for output validation
- [ ] Optional YAML output

## Contributing

Contributions, suggestions, and bug reports are welcome. Open an issue or submit a pull request.

## License

This project is licensed under the **GNU General Public License v3.0**. See [LICENSE](LICENSE) for full terms.

---

© 2025 Jaco <your name or handle>
