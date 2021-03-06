# Notes
A simple Zsh script to edit and manage synchronized notes (via a Git repository) on one or across many machines. [See the source](bin/notes).

## Installation
Clone the repository somewhere (e.g., `~/.src/notes`) and add `source $HOME/.src/notes/notes.zsh` to your `~/.zshrc`.

## Setup

### Configuration
* Set `NOTES_DIR` if you want a different notes path.  **Default is `~/.notes`.**
* Set `EDITOR` as your CLI text editor (if not already set).

### Notes Repository
Create a Git repository at `NOTES_DIR` (with a default remote).

**Warning: If you are planning to store sensitive information with `notes` do not make your notes repository public.**

## Usage

```Shell
$ notes             # Edits the default note (e.g., ~/.notes/notes)
$ notes <note-name> # Edits <note-name>      (e.g., ~/.notes/git-tips)
$ notes ls          # Lists all notes
```

Synchronization will happen before (`git pull`) and after (auto commit and `git push`) each editing of any note.

## Credits
Erik Nomitch: erik@nomitch.com
