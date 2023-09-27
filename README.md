# Buku Userscript for Qutebrowser

This is a [userscript](https://qutebrowser.org/doc/userscripts.html) for [Qutebrowser](https://qutebrowser.org) that integrates the [buku](https://github.com/jarun/buku) bookmark manager

## Install

```bash
wget -qO- https://raw.githubusercontent.com/spectronp/qutebrowser-buku/main/installer | bash
```

## How to set alias

### Run in Qutebrowser

`:config-dict-add aliases bk 'spawn --userscript buku'`

OR

### Add to config.py

```python
config.load_autoconfig()

c.aliases = config.get('aliases')
c.aliases['bk'] = "spawn --userscript buku"
```

## Usage

```
Usage:
    bk [url] [tag..]
    bk add [url] [tag...]
    bk open [-n NUM] ([-s | -S] <query>)
    bk open <index | index_range>
    bk edit <index> [edit data]
    bk del <index>
```

## Features
- [x] Basic CRUD
- [x] Open bookmarks with query
- [ ] Add all open tabs
- [ ] Better error feedback
- [ ] Support to buku search options
- [ ] Support to IPs and hostnames
- [ ] Confirmation dialog for delete and edit
- [ ] Use of a query in place of index ( edit and delete )
- [ ] Sync
- [ ] Support encrypted databases
