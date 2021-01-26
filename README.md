## bookmark.txt

If you're not familiar with `todo.txt`, see [here](https://github.com/todotxt/todo.txt#todotxt-format)

This is a thin wrapper around [`todo.txt`](https://github.com/todotxt/todo.txt-cli) to keep track of my bookmarks. All commands (except the `-d` flag) call the underlying todo.sh command.

It maintains a separate config file at `~/.config/bookmark.txt`. To change that, you can set the `BOOKMARK_CONFIG_DIR` environment variable and modify the generated config file.

---

### Usage

Like todo.txt, you can use flags to filter by multiple contexts/tags.

```bash
$ bookmark list +programming
1 programming; language theory http://alvaro-videla.com/archive.html +programming
--
BOOKMARKS: 1 of 3 tasks shown
```

Like `todo.txt`, its easy to create scripts on top of this since the data format is just a text file.

- [prompt](https://sean.fish/d/todo-prompt) - uses `rofi` to prompt me to add/mark bookmarks as 'done' (remove them)
- [open](https://sean.fish/d/bookmark-open) - uses `rofi` and [`urlextract`](https://pypi.org/project/urlextract/) on the selected bookmark, to open it in my browser

---

### Install

To install, copy the `bookmark` script onto your `$PATH` somewhere. To automate:

`sh <(curl -sSL http://git.io/sinister) -u 'https://raw.githubusercontent.com/seanbreckenridge/bookmark.txt/master/bookmark'`
