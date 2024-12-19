# TaskManagerCLI: A Simple Command-Line Task Manager

A lightweight and efficient command-line interface (CLI) application for managing your tasks.  Easily add, delete, list, and update tasks with simple commands.

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)


## Project Overview

TaskManagerCLI is designed to help you manage your daily tasks efficiently from your terminal.  It allows you to create tasks with titles, due dates, priorities, and notes, and then easily view, delete, and update them. This project is ideal for users who prefer a simple, text-based interface for task management.

**Key Features:**

* **Add Tasks:** Create new tasks with title, due date, priority (low, medium, high), and notes.
* **List Tasks:** View all tasks, optionally filtering to show only specific tasks.
* **Delete Tasks:** Remove completed or irrelevant tasks.
* **Update Tasks:** Modify existing tasks (not yet implemented in this version).


**Problem Solved:**  Provides a simple and efficient way to manage tasks without relying on complex graphical interfaces or web applications.

**Use Cases:**

* Quickly jot down and track daily tasks.
* Manage project to-do lists from the command line.
* Simple task management for users who prefer a terminal-based workflow.


## Table of Contents

* [Project Title and Short Description](#project-title-and-short-description)
* [Project Overview](#project-overview)
* [Prerequisites](#prerequisites)
* [Installation Guide](#installation-guide)
* [Usage Examples](#usage-examples)
* [Project Architecture](#project-architecture)
* [Contributing Guidelines](#contributing-guidelines)
* [License](#license)


## Prerequisites

* Go 1.18 or higher installed on your system.


## Installation Guide

1. **Clone the repository:**
   ```bash
   git clone https://github.com/harshkasat/taskManagerCli.git
   cd taskManagerCli
   ```

2. **Build the application:**
   ```bash
   go build
   ```

This will create an executable file (named `taskManagerCli` by default) in the current directory.


## Usage Examples

**Add a Task:**

```bash
./taskManagerCli add --title "Buy groceries" --priority high --notes "Milk, eggs, bread"
```

This adds a high-priority task titled "Buy groceries" with the specified notes.  If no due date is specified, it defaults to 7 days from the current date.

**List All Tasks:**

```bash
./taskManagerCli list -a
```
This lists all tasks with their ID, title, priority, notes, due date, and status.

**Delete a Task:**

```bash
./taskManagerCli del --id 1 
```

This deletes the task with ID 1.  (You need to list tasks first to find the ID).


## Project Architecture

The project uses the Cobra library for creating the CLI structure.  It uses JSON files (`task.json`) to store task data persistently.  The application consists of several commands (add, list, delete) handled by separate Go files.


## Contributing Guidelines

Contributions are welcome! Please open an issue to discuss proposed changes before submitting a pull request.


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


##  Future Roadmap

* Implement task updating functionality.
* Add search functionality to list tasks.
* Improve error handling and user feedback.
* Add support for different task storage methods (e.g., databases).

