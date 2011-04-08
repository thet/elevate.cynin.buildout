elevate cynin setup
===================

necessary ubuntu packages to install
------------------------------------
eventually install:
$ sudo apt-get install build-essential libssl-dev libjpeg62-dev libreadline5-dev wv  libxml2-dev libxslt1-dev libsasl2-dev poppler-utils libdb4.4-dev libldap2-dev python2.4-dev


get it
======
r/w access:
$ git clone git@github.com:thet/elevate.cynin.buildout.git

ro access:
$ git clone git://github.com/thet/elevate.cynin.buildout.git


installation
============

$ svn co http://odn.cynapse.com/svn/cynin/tags/cynin_3_2_2
$ python24 bootstrap.py -d -c base.cfg

on development box
------------------
$ ./bin/buildout -c base.cfg

on deployment box
-----------------
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
