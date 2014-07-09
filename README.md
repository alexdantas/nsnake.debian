# nsnake.debian

This repository contains the **Debian packaging files** for the game
Nsnake (_classic snake game with textual interface_).

If you're after the game Nsnake itself, [go to it's homepage][home]

![screen](http://nsnake.alexdantas.net/images/large-maze-with-lots-of-fruits.png)

## Debian Packaging

### Structure

* [**Nsnake on Debian Package Tracking System**][package]

This package is maintained on a Git repository through some important branches.

| branch                                                                            | role |
| --------------------------------------------------------------------------------- | ---- |
| [**master**](https://github.com/alexdantas/nsnake.debian/tree/master)            | Nsnake _and_ the debian package source code (`debian` directory) |
| [**upstream**](https://github.com/alexdantas/nsnake.debian/tree/upstream)        | Everything that was on the original upstream tarball (`orig.tar.gz`) |
| [**pristine-tar**](https://github.com/alexdantas/nsnake.debian/tree/pristine-tar)| Debian original tarball |
| [**readme**](https://github.com/alexdantas/nsnake.debian/tree/readme)            | This single file, explaining all that |


### Getting Started

To start working on this package, clone this repository
 [along with all branches](http://stackoverflow.com/a/72156):

```bash
# Cloning the entire repository
$ git clone https://github.com/alexdantas/nsnake.debian

# For now you have only the `readme` branch
$ git branch
* readme

# But the other branches are actually "hidden"
$ git branch -a
* readme
remotes/origin/master
remotes/origin/pristine-tar
remotes/origin/upstream

# So start working on one of them with this
# specific command:
$ git checkout -b master origin/master

# And by this moment you have this branch as "non-hidden"
# You can go back and forth as you like
$ git checkout -b readme
$ git checkout -b master
```

### Notes

1. Remember that the **master** is _not_ the one you get
   right after cloning this repository!
2. [Workaround.org has a nice article][article] on co-maintaining
a Debian package with Git and `git-buildpackage`.

[home]:    http://nsnake.alexdantas.net/
[package]: https://packages.qa.debian.org/n/nsnake.html
[article]: https://workaround.org/debian-git-comaintenance
