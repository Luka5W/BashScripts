# BashScripts
A bunch of bash utilities I use...

Every file is licensed under the Unlicense license, so do whatever you want.

## SetupGit

[file](./setupgit)

_A small script to setup a git repository with predefined email and username._


### Description

The names have to be defined by the user itself in the case statement.


### Usage

`setupgit [name] [y]`
When the `y`-flag is passed, git init will be called before setup


###Examples

```
$ setupgit lukas
$ setupgit lukas y
```


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

I haven't undestood, how you 'achieve' that, but it works for me, so… fixed. I
guess. So **use this script with caution**, if you know, what the author meant,
feel free to open an issue.


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
