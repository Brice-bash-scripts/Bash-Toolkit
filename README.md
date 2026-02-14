# 🛠 Bash Toolkit

A curated collection of production-quality Bash utilities for development, infrastructure, and filesystem automation.

This repository serves as a personal shell tooling library — focused on clarity, safety, portability, and maintainability.

---

## 🎯 Purpose

The goal of this repository is to:

- Build practical shell scripting fluency
- Maintain reusable infrastructure utilities
- Apply "strict mode" and defensive scripting practices
- Organize scripts by domain rather than by individual file
- Develop tooling that supports backend, ML, and infrastructure workflows

This is not a random script dump.
It is a structured automation toolkit.

---

## 📂 Repository Structure

```plaintext
bash-toolkit/
├── scripts/
│   ├── git/            # Git-related utilities
│   ├── venv/           # Virtual environment helpers
│   ├── filesystem/     # Filesystem automation scripts
│   └── misc/           # General utilities
│
├── lib/                # Shared helper functions (if needed)
├── docs/               # Documentation and design notes
└── README.md
```

Scripts are organized by functional domain to maintain clarity as the toolkit grows.

---

---

## ⚙️ Script Standards

All scripts in this repository follow these conventions:

### Shebang

    #!/usr/bin/env bash

### Strict Mode

    set -euo pipefail

---

## 🧱 Design Principles

- Defensive checks before modification
- Clear usage documentation at the top of each file
- Meaningful exit codes (`0` for success, non-zero for failure)
- Safe quoting practices (`"$variable"`)
- Minimal external dependencies
- Predictable and explicit behavior
- Prefer readability over clever one-liners
- Follow the Unix philosophy: small tools, well-composed

---

## 🚀 Usage

Most scripts are intended to be executed directly:

```bash
    chmod +x scripts/git/add_gitkeep_to_empty_dirs.sh
    ./scripts/git/add_gitkeep_to_empty_dirs.sh
```

Optionally, scripts may be added to your `$PATH`:

```bash
    export PATH="$PATH:/path/to/bash-toolkit/scripts"
```

---

## 🛡 Safety Expectations

Scripts that modify files or directories should:

- Validate execution context when necessary
- Avoid modifying system or hidden directories unintentionally
- Return proper exit codes for automation compatibility
- Support future dry-run modes where appropriate

---

## 📌 Future Improvements

- Add dry-run support to modification scripts
- Add logging helpers
- Introduce shared utility library under `/lib`
- Add lightweight test harness for critical scripts
- Expand into DevOps-style automation utilities

---

## 👤 Author

Brice  Nelson  
Backend & Applied ML Engineer  
Building practical automation muscle alongside Python systems.
