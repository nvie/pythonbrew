Overview
========

pythonbrew is a program to automate the building and installation of Python in the users HOME.

pythonbrew is based on `perlbrew <http://github.com/gugod/App-perlbrew>`_.

Installation
============

Following python version is required to use pythonbrew:
 2.4 <= Python < 3

The recommended way to download and install pythonbrew is to run these statements in your shell.::

  curl -LO http://github.com/utahta/pythonbrew/raw/master/pythonbrew-install
  chmod +x pythonbrew-install
  ./pythonbrew-install

After that, pythonbrew installs itself to ~/.pythonbrew, and you should follow the instruction on screen to setup your .bashrc or .cshrc to put it in your PATH.

If you need to install pythonbrew into somewhere else, you can do that by setting a PYTHONBREW_ROOT environment variable.::

  export PYTHONBREW_ROOT=/path/to/pythonbrew
  ./pythonbrew-install

Usage
=====

pythonbrew command [options]
    
Install some Pythons::

  pythonbrew install 2.6.6
  pythonbrew install Python-2.5.5
  pythonbrew install --configure="CC=gcc_4.1" Python-2.6.6
  pythonbrew install --no-setuptools Python-2.6.6
  pythonbrew install http://www.python.org/ftp/python/2.7/Python-2.7.tgz
  
Switch python in the $PATH::

  pythonbrew switch 2.6.6
  pythonbrew switch Python-2.5.5

List the available install versions of Python::

  pythonbrew list 2.6
  pythonbrew list 3.0

Uninstall some Pythons::

  pythonbrew uninstall 2.6.6

Remove stale source folders and archives::

  pythonbrew clean

Upgrades pythonbrew to the latest version::

  pythonbrew update

Disable pythonbrew::

  pythonbrew off

Show version::

  pythonbrew version

COMMANDS
========

install <version>
  Build and install the given version of Python.
  
  Setuptools and pip is automatically installed.
  
  options: --force, --no-setuptools and --configure.

installed
  List the installed versions of python.

switch <version>
  Switch to the given version.

list <version>
  List the available install version of python.
  
uninstall Python-<version>
  Uninstall the given version of python.

clean
  Remove stale source folders and archives.

update
  Upgrades pythonbrew to the latest version.

off
  Disable pythonbrew.

version
  Show version.

Options
=======

\-f | --force
  Force installation of a Python.

\-C | --configure
  Custom configure options.

\-n | --no-setuptools
  Skip installation of setuptools.
