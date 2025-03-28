# git-pr

A streamlined CLI tool for creating GitHub pull requests from the command line. This script automates the common workflow of creating a branch, committing changes, pushing to GitHub, and provides a direct link to create a pull request.

## Features

- 🌿 Create and switch to new branches
- 💾 Stage and commit all changes
- 🚀 Push to GitHub
- 🔐 GPG sign commits automatically (-S flag)
- 🔄 Force push option available
- 🎨 Colored and formatted terminal output
- 🔗 Direct link to create PR on GitHub

## Installation

1. Clone this repository or download the `git-pr` script
2. Make the script executable:
   ```bash
   chmod +x git-pr
   ```
3. Move or symlink the script to a directory in your PATH (e.g., `/usr/local/bin/` or `~/bin/`):
   ```bash
   mv git-pr /usr/local/bin/
   ```

## Usage

```bash
git pr [options]
```

### Options

- `-b, --branch BRANCH` - Specify the branch name
- `-m, --message MESSAGE` - Specify the commit message
- `-n, --no-push` - Skip pushing to remote
- `-f, --force` - Force push to remote

### Interactive Mode

If you don't provide the branch name or commit message through options, the script will prompt you for them interactively.

### Examples

Create a new branch and PR with options:
```bash
git pr -b feature/new-feature -m "Add new feature"
```

Create a PR interactively:
```bash
git pr
```

Force push to an existing branch:
```bash
git pr -b existing-branch -m "Update feature" -f
```

## Notes

- The script automatically converts SSH GitHub URLs to HTTPS URLs for the PR creation link
- All changes in the working directory will be staged and committed
- Commits are automatically signed (requires GPG setup)
- Colored output helps distinguish different types of information

## Requirements

- Git
- Bash
- A GitHub repository with proper remote setup
- GPG setup for commit signing
