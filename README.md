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

### Issues after update?
if `ppurge --version` still shows the old version after a refresh, it's likely a **PATH priority**
or **caching** issue.
1. **Clear the shell cache**:
Your terminal might still remember the old location of the script. Run this to reset it:
```bash
hash -r
```
2. **Check your PATH**:
Ensure your local bin directory is at the beginning of your `$PATH`. Add this to your ``.bashrc``:
```bash
export PATH="$HOME/.local/bin:$PATH"
```
Then apply the changes:
```bash
source .bashrc
```
3. **Remove old global versions**:
if you previously installed ``ppurge`` using ``sudo``, the old version in ``/usr/local/bin`` might be
overriding your local one. Remove it:
```bash
sudo rm /usr/local/bin/ppurge
```

## Requirements
* Python 3.11 or higher
* `colorama` library
* Have installed `git` on your system

## Contributing
Contributions are welcome! If you'd like to help improve **ppurge**, please read the [CONTRIBUTING.md](CONTRIBUTING.md) file to understand how to get started, report bugs, or submit your own pull requests.