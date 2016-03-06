BLOCKMON INSTALLATION INSTRUCTIONS
===================================

EXTERNAL LIBRARIES
------------------

PORTABILITY
-------------
Developed on Linux.

INSTALL
--------

1. Follow blockmon installation manual

2. Mount source rta/usr block to blockmon build space, f.i.:

  sudo mount --bind /home/aelz/samples/gitRepos/rta/usr/app_aelz /home/aelz/samples/gitRepos/blockmon/usr/app_aelz

3. Build and execute added plugin from blockmon workspace:

  cd ../blockmon
  cmake .
  cmake -DWITH_DAEMON=ON
  make
  cd daemon
  sudo python cli.py


ERRORS
------

1. Symbolic link as alternative install:
  cd blockmon/usr
  ln -s -t . /home/aelz/samples/gitRepos/rta/usr/app_aelz

Error: symbolic link ignored by blockmon cmake, so could require and additional investigation.
-----

