# 🚀 StackCraft

An interactive TUI to bootstrap project environments in seconds.

## Overview

StackCraft is a terminal app built with Go. When you run it, it updates your system package manager, checks that `git` and `nvim` are installed, and shows a menu to pick your tech stack. After you choose, it creates the project structure, installs dependencies, initializes Git and opens your editor.

## Features

- Interactive menu with keyboard navigation (Bubbletea + Lipgloss)
- Automatic package updates (`brew update` / `apt update`)
- Checks for `git` and `nvim` and installs them if missing
- Ready-made stacks:
  - **MERN**: Node.js, Express, React, MongoDB tools
  - **MARN**: Node.js, Express, Angular, MongoDB tools
  - **Python Backend**: venv, FastAPI, Uvicorn, SQLAlchemy
  - **Go REST API**: Go module, Chi Router, PGX driver
- Initializes a Git repository and opens `nvim` when done

## Requirements

- Go 1.20 or higher (to build from source)
- Linux, macOS or Windows via WSL
- Homebrew (`brew`) or APT (`apt`)
- `sudo` access

## Installation

```bash
git clone https://github.com/your-username/stackcraft.git
cd stackcraft
go build -o stackcraft .
sudo mv stackcraft /usr/local/bin/
```

## Usage

Go to an empty directory and run:

```bash
stackcraft
```

| Key | Action |
|-----|--------|
| `↑` / `k` | Move up |
| `↓` / `j` | Move down |
| `Enter` | Select stack and start setup |
| `q` / `Ctrl+C` | Quit |

## Project Structure

```
stackcraft/
├── main.go       # TUI model, views and stack installers
├── syscheck.go   # Package updates and tool checks
├── go.mod        # Go module
└── README.md
```

## Contributing

1. Fork the project
2. Create a branch (`git checkout -b feature/AddAwesomeStack`)
3. Commit your changes (`git commit -m 'Add Awesome Stack template'`)
4. Push the branch (`git push origin feature/AddAwesomeStack`)
5. Open a Pull Request

## License

MIT License. See `LICENSE` for details.
