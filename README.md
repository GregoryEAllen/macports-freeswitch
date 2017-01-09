# MacPorts - FreeSWITCH

This is a repository for developing a MacPorts interface (Portfiles) for installing FreeSWITCH, an open source telephony platform.

## MacPorts development repo

During development, I install a non-root MacPorts development repository in my home directory at `~/macports-dev`. Be sure that any other MacPorts installations are not in the path, so that they don't interfere with one another.

Download the MacPorts source installer, and configure it with:

    ./configure --prefix=/Users/gallen/macports-dev --with-applications-dir=~/macports-dev/Applications --with-install-user=$(id -u -n) --with-install-group=$(id -g -n) --with-no-root-privileges

Then build and install with:

    make
    make install

After installation, you must also tell macports where to find this repository by editing
`~/macports-dev/etc/macports/sources.conf` and adding a line like `file:///Users/gallen/repositories/macports-freeswitch`.
