# [st](https://github.com/NickoEgor/st) - the simple (suckless) terminal

The [suckless terminal (st)](https://st.suckless.org/) with patches

## Patches
+ [alphaFocusHighlight](https://st.suckless.org/patches/alpha_focus_highlight/): transparency patch with different alphas for focused/unfocused st
+ [bold-is-not-bright](https://st.suckless.org/patches/bold-is-not-bright/): disables "bright bold colors" behaviour in st
+ [clipboard](https://st.suckless.org/patches/clipboard/): copies selected text (with mouse) to clipboard and pastes it with middle-click
+ [externalpipe](https://st.suckless.org/patches/externalpipe/): read and write st's screen through a pipe
+ [keyboard\_select](https://st.suckless.org/patches/keyboard_select/): select text in st with keyboard
+ [several scrollback patches](https://st.suckless.org/patches/scrollback/): scrollback with keyboard and mouse
+ [vertcenter](https://st.suckless.org/patches/vertcenter/)
+ [xresources](https://st.suckless.org/patches/xresources/): adds Xresources support

## Bindings

+ Scrollback:
    - `alt-k/j` or `alt-↑/↓` - scroll by one line
    - `alt-u/d` or `alt-pageup/pagedown` - scroll by page
+ Zoom:
    - `alt-shift-k/j` or `alt-shift-up/down` - zoom font
    - `alt-shift-u/d` or `alt-shift-pageup/pagedown` - zoom larger
    - `alt-shift-r` or `alt-home` - returns to default
+ Copy text: `ctrl-shift-c`
+ Paste text:
    - `ctrl-shift-v` or `shift-insert` - clipboard
    - `ctrl-shift-p` - primary selection
+ Follow url: `alt-o`
+ Copy url: `alt-y`

## Installation

```
git clone https://github.com/NickoEgor/st
cd st
sudo make install
```

## Dependencies

+ `make`
+ `fontconfig` — system fonts
+ [`xurls`](https://github.com/mvdan/xurls) — parse urls (maybe get rid later)
+ `dmenu` — open/copy urls

## Troubleshoot
If `Delete` key doesn't work, put this in your `~/.inputrc` file:

```
set enable-keypad on
```
