# ppurge

---

`ppurge` is a lightweight Python automation script designed to help you recover from "oops" moments in Git. Accidentally pushed your entire Desktop or heavy junk files to a repo? `ppurge` cleans your history, resets the repository, and synchronizes the clean state—all in one command.

---

## Features
- **Nuke & Clean:** Automatically removes the entire Git history and local metadata to wipe out accidentally comitted sensitive data or junk files.
- **Smart Initialization:** Safely re-initializes the repository with a clean state.
- **Safety First:** Includes directory verification to ensure you don't accidentally nuke the wrong folder.
- **Visual Feedback:** Clean, colored status indicators (`[Info]`, `[Success]`, `[!]`) for better readability.
- **Self-Updating:** Built-in `--refresh` mechanism to keep your tool updated directly from Github.

## Usage
### `ppurge`
Initiates the cleanup process. It will prompt you for confirmation before deleting the local history and force-pushing the clean state to `origin main`.

### `--help`
Shows a list of commands

### `--refresh`
Fetch new version from this github repo.

### `--version`
Shows current version of ppurge.

## Setup
1. Clone this repo
   ```bash
   git clone https://github.com/wpxq/ppurge
   ```
2. Run the provided installation bash script:
   ```bash
   chmod +x ppurge_setup.sh
   ./ppurge_setup.sh
   ```


## Troubleshooting (PATH issues)
if the command is not found, add this to your `.bashrc` (or `.zshrc`):
```bash
export PATH="$HOME/.local/bin:$PATH"
```
### Then save and run: ```source .bashrc``` (or `source .zshrc`)

## Requirements
* Python 3.11 or higher
* `colorama` library
* Have installed `git` on your system

## Contributing
Contributions are welcome! If you'd like to help improve **ppurge**, please read the [CONTRIBUTING.md](CONTRIBUTING.md) file to understand how to get started, report bugs, or submit your own pull requests.