BULKSYNC
========

:Author: Christopher A. Snapp <snappca@gmail.com>
:Version: 16.02
:Copyright: GPLv3

**bulksync** executes rsync commands (optionally in parallel) based on a tracking file

.. contents::

Synopsis
--------

**bulksync** [**-dhv**] [**--help**] [**-c** *count*] [**-i** *input-directory*] [**-l** *log-directory*] [**-o** *output-directory*]


Description
-----------
bulksync provides a method for synchronizing the contents of a directory to
another existing directory in parallel with centralized control via a state
file.

The benefit of this approach is that you can have several machines referencing
the same state file and saturating your network through high concurrency.


Options
-------
    **-c** *count*
      the number of jobs to run concurrently; default is ``10`` if no value is
      provided

    **-d**
      enable debug mode (print ALL output)

    **-h, --help**
      display this help and exit

    **-i** *directory*
      the directory to sync FROM

    **-l** *directory*
      the directory where sync state and log output will be tracked

    **-o** *directory*
      the directory to sync TO

    **-v**
      display version information and exit

Installation
------------
    1. ensure rsync, lockfile-progs, and bulksync are in your ``$PATH``

Copyright
---------
Copyright (C) 2016, Christopher A. Snapp <snappca@gmail.com>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
