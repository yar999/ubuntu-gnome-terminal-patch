# Gnome Terminal Patch

Originally from [Tomba's Blog](http://www.taika.org/~tomba/gnome-terminal/index.html),
a patch to add PuTTY-like copy on select and right-click paste to Gnome Terminal in Ubuntu.

I built the patched version on Ubunty Trusty 14.04, Gnome Terminal 3.6.2.

## Building Instructions using Patch

1. Install build dependencies

```bash
sudo apt-get build-dep gnome-terminal
```

2. Download the sources and apply the patch

```bash
mkdir gnome-terminal
cd gnome-terminal
apt-get source gnome-terminal
cd gnome-terminal-3.6.2
patch -p1 < gnome-terminal.patch
```

3. Build

```bash
dpkg-buildpackage -us -uc -b
```

4. Install

```bash
cd ..
dpkg -i *.deb
```

## License

[MIT License](http://en.wikipedia.org/wiki/MIT_License)