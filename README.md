## bookmark.txt

If you're not familiar with `todo.txt`, see [here](https://github.com/todotxt/todo.txt#todotxt-format)

This is a thin wrapper around [`todo.txt`](https://github.com/todotxt/todo.txt-cli) to keep track of my bookmarks. All commands (except the `-d` flag) call the underlying todo.sh command.

It maintains a separate config file at `~/.config/bookmark.txt`. To change that, you can set the `BOOKMARK_CONFIG_DIR` environment variable and modify the generated config file.

Should mention that this works perfectly fine if your todo configuration is very simple, but if you start adding [third party add-ons](https://git.sr.ht/~proycon/todotxt-more) for `todo.txt`, it can be annoying to sync config changes. I've since come up with a better solution for myself, see [managing multiple todo.txt files](https://sean.fish/x/blog/managing-multiple-todo-txts/)

### Usage

Like todo.txt:

- you can use flags to filter by multiple contexts/tags.

```bash
$ bookmark list +programming
1 programming; language theory http://alvaro-videla.com/archive.html +programming
--
BOOKMARKS: 1 of 3 tasks shown
```

- its easy to create scripts on top of this since the data format is just a text file:
  - [prompt](https://sean.fish/d/todo-prompt) - uses `rofi` to prompt me to add/mark bookmarks as 'done' (remove them)
  - [open](https://sean.fish/d/bookmark-open) - uses `rofi` and [`urlextract`](https://pypi.org/project/urlextract/) on the selected bookmark, to open it in my browser

### Install

To install, copy the `bookmark` script onto your `$PATH` somewhere

Could use [`basher`](https://github.com/basherpm/basher) to do that for you:

```bash
basher install seanbreckenridge/bookmark.txt
```
