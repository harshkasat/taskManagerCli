# TaskManagerCLI: A Simple Command-Line Task Manager

A lightweight command-line interface (CLI) tool for managing your tasks.  Easily add, delete, update, and list your tasks.

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)


## Project Overview

TaskManagerCLI provides a simple and efficient way to manage your to-do list from your terminal.  It allows you to add tasks with titles, due dates, priorities, notes, and status, and then easily list, update, or delete them. This tool is perfect for individuals who prefer a command-line interface for task management or want a simple, no-frills solution.

## Table of Contents

* [Prerequisites](#prerequisites)
* [Installation](#installation)
* [Usage](#usage)
    * [Adding a Task](#adding-a-task)
    * [Listing Tasks](#listing-tasks)
    * [Updating a Task](#updating-a-task)
    * [Deleting a Task](#deleting-a-task)
* [Project Architecture](#project-architecture)
* [Contributing](#contributing)
* [License](#license)


## Prerequisites

* Go 1.18 or higher installed on your system.


## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/harshkasat/taskManagerCli.git
   cd taskManagerCli
   ```

2. **Build the application:**
   ```bash
   go build
   ```

This will create an executable file (named `task-manager` by default) in your current directory.


## Usage

The application is executed using the `task-manager` command followed by subcommands.

### Adding a Task

To add a new task, use the `add` subcommand.  You can specify the title, due date, priority, notes, and status.  All fields are optional except for the title.  Dates should be in YYYY-MM-DD format.

```bash
task-manager add --title "Write README" --due 2024-10-27 --priority high --notes "Important for release" --status pending
```

### Listing Tasks

To list all tasks, use the `list` subcommand.  Currently, this only lists all tasks.  Future versions may allow filtering.

```bash
task-manager list
```

### Updating a Task

To update a task, use the `update` subcommand, specifying the task ID, field to update, and new value.

```bash
task-manager update --id 1 --field title --new "Revised README"
```

This updates task with ID 1's title to "Revised README".  Fields that can be updated are: `title`, `due`, `priority`, `notes`, `status`.

### Deleting a Task

To delete a task, use the `del` subcommand, specifying the task ID.

```bash
task-manager del --id 1
```


## Project Architecture

The project uses the Cobra CLI library for Go.  It's structured with a `rootCmd` and subcommands for adding, listing, updating, and deleting tasks.  Task data is stored in a JSON file (currently not specified in the code).


## Contributing

Contributions are welcome! Please open an issue or submit a pull request.


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


**(Note:  The provided code lacks robust error handling and input validation.  The JSON file location for task storage is not defined.  The `all` flag in `listTask.go` and `root.go` appears to be intended for a different functionality and is not fully implemented.  These aspects should be improved for a production-ready application.)**
