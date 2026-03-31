# BashExplain

[![PyPI version](https://badge.fury.io/py/bashexplain.svg)](https://pypi.org/project/bashexplain/)
[![Python 3.6+](https://img.shields.io/badge/python-3.6+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Zero Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen.svg)]()

A command-line tool that explains Bash commands, terminal errors, and shell scripts in plain English. Lightweight, offline-first, and zero dependencies.

## Installation

### Recommended (pipx — for CLI tools)

```bash
pipx install bashexplain
```

### Alternative (pip)

```bash
pip install bashexplain
```

### From source

```bash
git clone https://github.com/singhashish12238-pixel/bash-explain.git
cd bash-explain
pipx install .
```

## Usage

### Explain a command

```bash
bashexplain command "ls -lah /home"
bashexplain command "grep -r 'TODO' ."
bashexplain command "tar -czf backup.tar.gz ~/documents"
```

### Explain an error

```bash
bashexplain error "bash: git: command not found"
bashexplain error "Permission denied"
bashexplain error "No such file or directory"
```

### Explain a script line by line

```bash
bashexplain script myscript.sh
```

## Features

### Command Explanation Engine
- 60+ common commands with plain-English descriptions
- Parses flags, arguments, pipes, and redirections
- Classifies argument types (absolute path, variable, glob pattern, etc.)

### Flag & Option Recognition
- 40+ common flag patterns (`-a`, `-r`, `-v`, `--help`, etc.)
- Infers meaning of unknown flags automatically

### Safety Warnings
- Detects 24+ dangerous command patterns
- Warns about destructive operations (`rm -rf /`, `chmod 777`, fork bombs)
- Flags unsafe download-and-execute patterns (`curl | bash`)
- Caution notices for `sudo` usage

### Error Explanation
- 10+ common terminal error patterns
- Plain-language explanation of what went wrong
- Common causes and step-by-step safe solutions

### Script Analysis
- Line-by-line breakdown of `.sh` scripts
- Explains variables, conditionals, loops, functions
- Detects shebang, comments, and control flow

### Designed for Safety
- Never executes any command — read-only analysis
- No root/sudo required
- Works completely offline
- Rule-based logic — no black box, fully transparent

## Technology

- **Language**: Python 3.6+
- **Dependencies**: None (standard library only)
- **Design**: OOP — `CommandExplainer`, `ErrorExplainer`, `ScriptExplainer`
- **Method**: Pattern matching and rule-based analysis

## Examples

```bash
$ bashexplain command "rm -rf /"

⚠️  SAFETY WARNINGS:
   DANGEROUS: This will delete files starting from root directory

🔧 Command: rm
   Remove files or directories
...
```

```bash
$ bashexplain error "Permission denied"

🔴 Error Message: Permission denied

📖 Explanation:
   You don't have permission to perform this operation.

🔍 Common Causes:
   1. File is not executable
   2. Insufficient user permissions
   ...
```

See [EXAMPLES.md](EXAMPLES.md) for full output examples across all three modes.

## Contributing

Contributions are welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on adding commands, error patterns, flags, and safety warnings.

## Authors

- Ashish Singh — [GitHub](https://github.com/singhashish12238-pixel)
- Ravi Poddar

## License

MIT License — see [LICENSE](LICENSE) for details.

## Acknowledgements

Some commands, flag descriptions, and error patterns in this project were developed 
with assistance from Claude (Anthropic) and GitHub Copilot. All code has been reviewed, 
tested, and understood by the authors.
