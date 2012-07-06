elevate cynin setup
===================

necessary ubuntu packages to install
------------------------------------

eventually install:

$ sudo apt-get install python2.6-dev

$ sudo apt-get install build-essential libreadline-dev zlib1g-dev libbz2-dev

$ sudo apt-get install libssl-dev libjpeg8-dev

$ sudo apt-get install wv libxml2-dev libxslt1-dev libsasl2-dev poppler-utils

$ sudo apt-get install libdb4.4-dev libldap2-dev

$ sudo apt-get install git subversion

$ addgroup --system zope
$ adduser --system --no-create-home --disabled-login --ingroup zope --disabled-password --shell /bin/false zope

install python 2.4
==================

Python 2.4 is not available on debian-stable, so you have to build it:

$ cd PYTHON_INSTALL_DIRECTORY

r/w access
----------

$ svn co https://svn.plone.org/svn/collective/buildout/bda-naked-python/

r/o access
----------

$ svn co http://svn.plone.org/svn/collective/buildout/bda-naked-python/

all
---

$ mkdir devsrc
$ cd devsrc/
$ git clone git@github.com:thet/buildout-base.git
$ cd ..


$ cd bda-naked-python24

$ python bootstrap.py -d -c buildout2.4.cfg

$ ./bin/buildout -c buildout2.4.cfg


get it
======

$ cd INSTALL_DIRECTORY

r/w access
----------

$ git clone git@github.com:thet/elevate.cynin.buildout.git

ro access
---------

$ git clone git://github.com/thet/elevate.cynin.buildout.git


installation
============

$ cd elevate.cynin.buildout

$ svn co http://odn.cynapse.com/svn/cynin/tags/cynin_3_2_2


on development box
------------------

$ PYTHON_INSTALL_DIRECTORY/bin/python24 bootstrap.py -d -c dev.cfg

$ ./bin/buildout -c dev.cfg


on deployment box
-----------------

$ PYTHON_INSTALL_DIRECTORY/bin/python24 bootstrap.py -d -c deployment.cfg

$ ./bin/buildout -c deployment.cfg


all
---

- login to management interface http://localhost:8080/manage

  user: admin

  pw: secret

- create a ZODB mount point

- add plone instance with id 'elevate_cynin' and product ubify.policy enabled



cynin resources
===============

http://www.cynapse.com/downloads/cynin-community-edition

http://odn.cynapse.com/svn/cynin/

http://odn.cynapse.com/svn/cynin/tags/cynin_3_2_2/

http://www.cynapse.com/community/home/cyn.in-developers/quickstart-buildout
