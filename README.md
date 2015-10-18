Axel’s No-Op Replacement Packages
=================================

These packages are solely there, because some (mostly GNOME related)
packages in Debian have hard dependencies on packages they don't
really need and hence need fake packages to satisfy these
dependencies.

Packages
--------

The repository contains source code for the following packages:

### colord

The sole purpose of this package is to fulfill gnome-control-center
3.8.x's silly dependency on colord which pulls in ConsoleKit and
PolicyKit which are usually unwanted on lean systems.

Should be named fake-colord, but that doesn't work until dpkg and apt
support versioned Provides (which they do since Jessie).

### fake-consolekit

The sole purpose of this empty dummy package is to fulfill
e.g. lxsession 0.5.x's but also other packages' unnecessary dependency
on consolekit.

### fake-accountsservice

The sole purpose of this empty dummy package is to fulfill
e.g. gnome-control-center's but also other packages' unnecessary
dependency on accountsservice.

APT Repository
--------------

All those metapackages are usually also available from
[my APT repository](http://noone.org/apt/).
