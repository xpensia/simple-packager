# Package manager for linux binaries

There is no goal to replace aptitude, yum or pacman.
This package manager aim to provide à simple way to build minimal linux system from a running distro.

It may be usefull for building small chroot system.

It's one of the base building block of xpensia's PaaS :)

> What looks like a cool idea at first may be stupid later. -- @JeanSebTr, writing a fraking package manager.

## xpensia-slp

The script name : `xpensia-slp`

General usage : `xpensia-slp [options] command [arguments...]`


## command _add_

Usage : `xpensia-slp add <file> [more files...] <package>`

Will add `file` to a new or existing `package`.
 * Add simple files as is
 * Add binary and check dependencies
 * Resolve library dependencies with `ldd`
 * Follow and preserve symlinks in the package


## command _show_

Usage : `xpensia-slp show <package>`

Show information about the `package`.
 * Meta data : md5, date ...
 * Dependencies
 * Version ?

## command _list_

Usage : `xpensia-slp list <package>`

Will list every file from `package`.


## command _install_

Usage : `xpensia-slp install <package>`

Will install the specified `package` on the system.
 * Resolve dependencies
 * Install the package and all the dependencies


## command _optimise_

Usage : `xpensia-slp optimise`

Special command for cache administration.
 * Read all the packages and the files they contain
 * Cross reference the files which are common to multiple packages
 * Build new packages from the common files
 * Add dependencies informations












