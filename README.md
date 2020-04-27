# [st](https://github.com/NickoEgor/st) - the simple (suckless) terminal

The [suckless terminal (st)](https://st.suckless.org/) with patches

## Patches

+ [alpha](https://st.suckless.org/patches/alpha/): transparency patch
+ [bold-is-not-bright](https://st.suckless.org/patches/bold-is-not-bright/): disables "bright bold colors" behaviour in st
+ [externalpipe](https://st.suckless.org/patches/externalpipe/): read and write st's screen through a pipe
+ [several scrollback patches](https://st.suckless.org/patches/scrollback/): scrollback with keyboard and mouse + [vertcenter](https://st.suckless.org/patches/vertcenter/)
+ [vertcenter](https://st.suckless.org/patches/vertcenter/): vertically center lines in the space available
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
    - `ctrl-shift-v` - clipboard
    - `ctrl-shift-p` or `shift-insert` - primary selection
+ Follow url: `alt-o`
+ Copy url: `alt-y`

## Installation

```
git clone https://github.com/NickoEgor/st
cd st
sudo make clean install
```

## Running

If you did not install st with make, you must compile
the st terminfo entry with the following command:
```
tic -sx st.info
```
See the man page for additional details.

## Dependencies

+ `fontconfig` — system fonts
+ [`xurls`](https://github.com/mvdan/xurls) — parse urls (maybe get rid later)
+ `dmenu` — open/copy urls

## Troubleshoot
If `Delete` key doesn't work, put this in your `~/.inputrc` file:

```
set enable-keypad on
```
