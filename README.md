grsec-slackware
===============
This is a script to automatically pull and build the Linux kernel patched with the latest grsecurity test version (and package it for Slackware). For simplicity, RBAC is disabled by default, but that can be easily changed.

Disclaimer
----------
Although I wanted an easy way to test and update grsecurity, I don't know shell scripting very well at all, and I made this as a learning exercise. So this may or may not work for you, and you first should know [whether or not you can run grsecurity on your system](https://en.wikibooks.org/wiki/Grsecurity). I'm pretty sure that this won't work on any system running proprietary graphics drivers (unless they're patched first).

