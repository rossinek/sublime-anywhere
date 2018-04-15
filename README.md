# sublime-anywhere

__Strongly inspired__ by [cknadler/vim-anywhere](https://github.com/cknadler/vim-anywhere).

*Note: Currently works only for macOS.*

Once [invoked](#keybinding), sublime-anywhere will create new temporary file with currently selected text. After close (and save) content of this file will be pasted into previously used application.

## Installation

#### Requirements

- Sublime (and `subl` executable)

#### Install

```bash
curl -fsSL https://raw.github.com/rossinek/sublime-anywhere/master/install | bash
```

#### Update

```bash
~/.sublime-anywhere/install
```

#### Uninstall

```bash
~/.sublime-anywhere/uninstall
```

## Keybinding

__macOS:__ ( default = `ctrl+cmd+v` )

You can adjust the shortcut via system preferences.

```
System Preferences > Keyboard > Shortcuts > Services > Sublime Anywhere
```

## History

Exactly the same like vim-anywhere, sublime-anywhere creates a temporary file in `/tmp/sublime-anywhere` when invoked. These files stick around until you restart your system, giving you a temporary history.

View your history:

```bash
$ ls /tmp/sublime-anywhere
```

Reopen your most recent file:

```bash
$ subl $( ls /tmp/sublime-anywhere | sort -r | head -n 1 )
```

## License

MIT
