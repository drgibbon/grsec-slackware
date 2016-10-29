grsec-slackware
===============
This script automatically pulls the latest grsecurity test version
with correct kernel version, applies the patch, and compiles. It then
creates a slackpkg (with kernel, source, modules, and firmware all in
one). The package should not clobber any base Slackware files.

For simplicity, RBAC is disabled by default, but that can be easily
changed. As is, the script won't run as root, and you need
[fakeroot](https://slackbuilds.org/repository/14.2/system/fakeroot/)
installed so the package can be created with proper root permissions
(you can pass `MANPO=no` to the fakeroot SlackBuild to avoid the
dependencies).

Usage
-----
Just clone the repo and run it;
```sh
git clone https://github.com/drgibbon/grsec-slackware.git
cd grsec-slackware
./grsec-slackware.SlackBuild
```

The slackpkg (not installed) will be created in /tmp

Disclaimer
----------
Although I wanted an easy way to test and update grsecurity, I don't
know shell scripting very well at all, and I made this largely as a
learning exercise. So this may or may not work for you, and you first
should know [whether or not you can run grsecurity on your
system](https://en.wikibooks.org/wiki/Grsecurity). I'm pretty sure
that this won't work on any system running proprietary graphics
drivers (unless they're patched first).

The kernel config is based on the Slackware 14.2 release, with all new
options set to module (if possible) or otherwise the default. I'm sure
this could be done better.