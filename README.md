🚀 StackCraft

An interactive TUI CLI to bootstrap, install dependencies, and setup project environments in seconds.

🌐 Read this documentation in Español.

📖 Overview

StackCraft is an interactive Terminal User Interface (TUI) built with Go that automates development environment setup with a single command.

When executed, it updates your system package manager, verifies core developer tools (git, nvim), and presents an interactive menu to choose your preferred tech stack (MERN, MARN, Python Backend, Go REST API, and more).

Once a stack is selected, StackCraft handles directory structure creation, virtual environment setup, dependency installation, Git initialization, and launches your text editor so you can start coding right away.

✨ Features

⚡ Interactive TUI: Smooth keyboard navigation powered by Bubbletea and styled with Lipgloss.

🔄 Auto Package Management: Runs system package updates (brew update / apt update) before displaying options.

🛡️ Environment Check & Idempotency: Automatically checks for core dev tools (like git and nvim) and installs missing dependencies via Homebrew or APT.

📦 Pre-configured Stacks:

MERN Stack: Node.js, Express, React, MongoDB tools.

MARN Stack: Node.js, Express, Angular, MongoDB tools.

Python Backend: Virtual environment (venv) setup with FastAPI, Uvicorn, and SQLAlchemy.

Go REST API: Module initialization with Chi Router and PGX driver.

🐙 Git & Editor Ready: Initializes a local Git repository and immediately launches nvim upon setup completion.

🛠️ Tech Stack & Requirements

Language: Go (Golang 1.20+)

TUI Engine: Bubbletea & Lipgloss (Charm.sh ecosystem)

Supported Platforms: Linux, macOS, and Windows Subsystem for Linux (WSL)

Package Managers: Homebrew (brew) or APT (apt)

🚀 Quick Start

1. Prerequisites

Ensure you have Go installed on your system. If you are using Linux/WSL with Homebrew:

brew install go


2. Installation

Clone the repository and build the binary:

# Clone the repository
git clone https://github.com/your-username/stackcraft.git
cd stackcraft

# Build the application
go build -o stackcraft .

# Move binary to PATH for global usage
sudo mv stackcraft /usr/local/bin/


💻 Usage

Navigate to any empty directory where you want to start a new project, then run:

stackcraft


Keyboard Shortcuts

↑ / k: Move cursor up

↓ / j: Move cursor down

Enter: Select stack and execute automated setup

q or Ctrl+C: Quit application

📁 Project Architecture

stackcraft/
├── syscheck.go   # Package updater & tool dependency verification
├── main.go       # Bubbletea TUI model, update cycle, views & stack installers
├── go.mod        # Go module definition
└── README.md     # Project documentation


🤝 Contributing

Contributions are welcome! If you want to add a new stack definition (e.g., Spring Boot, Rust, Laravel):

Fork the Project

Create your Feature Branch (git checkout -b feature/AddAwesomeStack)

Commit your Changes (git commit -m 'Add Awesome Stack template')

Push to the Branch (git push origin feature/AddAwesomeStack)

Open a Pull Request

📜 License

Distributed under the MIT License. See LICENSE for more information.
