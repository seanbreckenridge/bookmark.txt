## bookmark.txt

If you're not familiar with `todo.txt`, see [here](https://github.com/todotxt/todo.txt#todotxt-format)

This is a thin wrapper around [`todo.txt`](https://github.com/todotxt/todo.txt-cli) to keep track of my bookmarks. All commands (except the `-d` flag) call the underlying todo.sh command.

It maintains a separate config file to `todo.txt`, at `/home/sean/.config/bookmark.txt` (set `BOOKMARK_CONFIG_DIR` and modify the generated config file to edit)

---

### Install

To install, copy `bookmark` onto your `$PATH` somewhere. To automate:

`sh <(curl -sSL http://git.io/sinister) -u 'https://raw.githubusercontent.com/seanbreckenridge/bookmark.txt/master/bookmark'`
