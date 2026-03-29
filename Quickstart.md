# Quick Start Guide

Get up and running with BashExplain in 2 minutes!

## Installation

### Option 1: Install from PyPI (Recommended)

```bash
# Using pipx (best for CLI tools)
pipx install bashexplain

# Or using pip
pip install bashexplain
```

### Option 2: Quick Download (No install needed)

```bash
# Download the script
curl -O https://raw.githubusercontent.com/singhashish12238-pixel/bash-explain/main/bash_explain.py

# Try it out!
python3 bash_explain.py command "ls -la"
```

### Option 3: Clone Repository (For contributors)

```bash
git clone https://github.com/singhashish12238-pixel/bash-explain.git
cd bash-explain
pipx install .
```

## Basic Usage

### 1. Explain a Command

```bash
bashexplain command "grep -r 'TODO' ."
```

**What you'll see:**
- Command name and purpose
- Explanation of each flag
- What each argument means
- Safety warnings (if applicable)

### 2. Understand an Error

```bash
bashexplain error "Permission denied"
```

**What you'll see:**
- Plain language explanation
- Common causes
- Step-by-step solutions

### 3. Analyze a Script

```bash
bashexplain script myscript.sh
```

**What you'll see:**
- Line-by-line breakdown
- Explanation of variables
- Control flow explanation
- Command usage

## Common Commands to Try

```bash
# File operations
bashexplain command "cp -r source/ dest/"
bashexplain command "find . -name '*.log' -delete"

# Text processing
bashexplain command "cat file.txt | grep error | wc -l"

# Git operations
bashexplain command "git log --oneline --graph --all"

# System administration
bashexplain command "sudo systemctl restart nginx"

# Docker
bashexplain command "docker run -it --rm ubuntu bash"
```

## Common Errors to Try

```bash
bashexplain error "command not found"
bashexplain error "Permission denied"
bashexplain error "No such file or directory"
bashexplain error "syntax error near unexpected token"
```

## Tips

### 1. Use Quotes for Complex Commands

```bash
# Good
bashexplain command "ls -la | grep txt"

# Won't work as expected
bashexplain command ls -la | grep txt
```

### 2. Check Before You Execute

```bash
# Before running an unfamiliar command, understand it first
bashexplain command "rm -rf node_modules"
```

### 3. Learn from Errors

```bash
# When you get an error, understand it
bashexplain error "bash: ./script.sh: Permission denied"
```

### 4. Combine with Other Tools

```bash
# First understand, then execute
bashexplain command "tar -czf backup.tar.gz ~/documents"
tar -czf backup.tar.gz ~/documents
```

## Next Steps

1. **Read the full README** for detailed features
2. **Check EXAMPLES.md** for more use cases
3. **Star the repository** if you find it helpful
4. **Contribute** by adding commands, errors, or features
5. **Share** with others who are learning Linux

## Getting Help

- Run `bashexplain --help` for CLI help
- Check the [GitHub Issues](https://github.com/singhashish12238-pixel/bash-explain/issues)
- Read the [full documentation](README.md)

Happy learning! 🚀