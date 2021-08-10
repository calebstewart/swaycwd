# swaycwd

This is similar to the [`xcwd`](https://github.com/schischi/xcwd) tool which prints the current working directory of the focused window on X.Org. This application will simply find the deepest child of the focused node, and print it's current working directory.

In the case of shells, this should allow you to easily spawn a new shell in the CWD if your shell does not provide the functionality natively. This is also useful so that you can have one keyboard shortcut which always opens a terminal regardless of what is open intelligently.

## Dependencies

You will need `jq` and `gron` and you will also need to be using `swaywm`.

```sh
# Install jq on Arch
pacman -S jq
# gron is available in the AUR
yay -S gron
```

## Usage

```
# Get the cwd of the active window
$ swaycwd
/home/caleb/git/swaycmd
# Start a shell in the cwd of the focused window
$ alacritty --working-directory="$(swaycwd)"
```
