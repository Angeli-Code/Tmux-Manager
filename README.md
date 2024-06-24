# Tmux Manager

Tmux Manager is a script that helps you manage Tmux sessions and navigate your projects with ease. It provides an interactive menu to create, attach, detach, and kill Tmux sessions, as well as navigate your file system and git repositories using `fzf`.

## Features

- **Create Tmux Sessions**: Start a new Tmux session from any directory or from a list of git repositories.
- **Attach to Sessions**: Easily attach to existing Tmux sessions.
- **Detach from Sessions**: Detach from the current Tmux session.
- **Kill Sessions**: Kill specific Tmux sessions or all sessions.
- **Open Repository**: Open the Tmux Manager repository in your default web browser.
- **Toggle Help**: Display command help in the menu.
- **Detailed Help**: Access detailed help documentation within the script.

## Requirements

- Tmux
- `fzf`
- `xdg-open` (or `open` on macOS)

## Installation

1. Ensure you have Tmux and `fzf` installed.
2. Download the `tmmux` script and make it executable:

    ```sh
    chmod +x tmmux
    ```
3. Move the script to /usr/local/bin

    ```sh
    sudo mv tmmux /usr/local/bin
    ```
## Usage

Run the script with:

```sh
tmmux
```

### Menu Options

- **'c'**: Create a new Tmux session from a general directory selection (root directory).
- **'p'**: Create a new Tmux session from a list of git repositories (within your home directory).
- **'a'**: Attach to an existing Tmux session.
- **'d'**: Detach from the current Tmux session.
- **'k'**: Kill an existing Tmux session.
- **'r'**: Open the Tmux Manager repository URL.
- **'q'**: Quit the program.
- **'t'**: Toggle the command help display.
- **'h'**: Display detailed help documentation.

## How the Script Works
The Tmux Manager script is designed to help you manage your Tmux sessions efficiently. Below is a detailed explanation of its functionality:
Overview

The script provides an interactive menu that allows you to create, attach, detach, and kill Tmux sessions. It also includes features to navigate your file system and git repositories using fzf (a command-line fuzzy finder).
Key Components

    Configuration File:
        The script uses a configuration file ($HOME/.tmux_manager_config) to save user preferences, such as whether to display help messages.

    Projects File:
        The script maintains a list of git repositories in a file ($HOME/Management/projects.txt) for quick access.

    Interactive Menu:
        The main menu is displayed in the terminal and provides various options for managing Tmux sessions.

Commands and Options

    Create Tmux Session (c):
        Prompts the user to select a directory from the root (/) using fzf.
        The user then provides a session name, and a new Tmux session is created in the selected directory.

    Create Tmux Session from Git Repositories (p):
        Updates the list of git repositories within the user's home directory.
        Prompts the user to select a repository using fzf.
        The user then provides a session name, and a new Tmux session is created in the selected repository.

    Attach to Existing Session (a):
        Lists all active Tmux sessions.
        Prompts the user to select a session by number to attach to it.

    Detach from Current Session (d):
        Detaches from the current Tmux session.

    Kill Existing Session (k):
        Lists all active Tmux sessions.
        Prompts the user to select a session by number to kill it, or choose 'a' to kill all sessions.

    Open Repository URL (r):
        Opens the Tmux Manager GitHub repository in the default web browser for more information and access to the source code.

    Quit Program (q):
        Exits the script and returns to the terminal.

    Toggle Command Help Display (t):
        Toggles the display of command help in the main menu.

    Display Detailed Help (h):
        Shows a detailed help screen with information about all commands and usage instructions.

Additional Features

    Dynamic Updates:
        The script dynamically updates the list of git repositories to ensure the latest information is available.

    Error Handling:
        Basic error handling is implemented to manage invalid inputs and ensure smooth operation.

    User Feedback:
        Clear messages are provided for actions like creating sessions, changing directories, and selecting projects.

By integrating these features, the Tmux Manager script provides a comprehensive tool for managing Tmux sessions and navigating projects with ease.

## Detailed Help

For more detailed information, press 'h' within the script to access the help documentation. You can also type 'r' to open the repository URL, which includes the source code and README for additional details.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests on the [repository](https://github.com/Angeli-Code/tmux-manager).

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
