# BashScripts
A bunch of bash utilities I use...

Every file is licensed under the Unlicense license, so do whatever you want.

## KDE Plasma Window Mover

[file](./kwin-mv-activity)

_A small script to move a window to another activity._

I've written the script because it annoyed me that it is not possible to move a
window to another activity with a shortcut. See
[this bug report](https://bugs.kde.org/show_bug.cgi?id=459961). My script is
based on _avalonvales_ commands. **Thank you** at this point, if you're reading
this.


### A word of WARNING:

The author of the issue wrote:

> But hopefully you can see why this implementation is really messy (you can
> send your desktop to the shadow realm if you're not careful). \[…\]

This shoud've been fixed in v0.0.2.


### Description

Currently, the only ways to move windows to another activities are by opening
the window menu (`Ctrl+F3` » Show in Activities) or by adding the activity to
the panel and dragging the window on it.

This can be automated by downloading this script and adding a shortcut with a
command to it.

### (Roughly) tested under

|                        |               |
|:-----------------------|:--------------|
| Operating System       | Kubuntu 22.04 |
| KDE Plasma Version     | 5.24.7        |
| KDE Frameworks Version | 5.92.0        |
| Qt Version             | 5.15.3        |
| Graphics Platform      | X11           |

(Just use it how it's intended, I haven't cached every edge case)


## Merge-Scanned-Docs

_A quick and dirty utility to fit
`pdftk A="$inA" B="$inB" shuffle A Bend-1 output "$out"` into a single command._

### Requirements

The script requires [pdftk](https://packages.debian.org/buster/pdftk).

(Debian based: `sudo apt install pdftk`)

(Man Page:
[pdftk(1)](https://manpages.debian.org/stretch/pdftk/pdftk.1.en.html))


### Usage

`merge-scanned-docs /path/to/file`

The script expects two files: `/path/to/file_odd.pdf` which contains the odd
pages and `/path/to/file_even.pdf` which contains the even pages.
And it expects that `/path/to/file.pdf` does not exist.

If no argument is passed, it prints a help text and exits.


## SetupGit

[file](./setupgit)

_A small script to setup a git repository with predefined email and username._


### Description

The names have to be defined by the user itself in the case statement.


### Usage

`setupgit [name] [y]`
When the `y`-flag is passed, git init will be called before setup


### Examples

```
$ setupgit lukas
$ setupgit lukas y
```
