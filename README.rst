elevate cynin setup
===================

necessary ubuntu packages to install
------------------------------------

eventually install::

    $ sudo apt-get install python2.6-dev
    $ sudo apt-get install build-essential libreadline-dev zlib1g-dev libbz2-dev
    $ sudo apt-get install libssl-dev libjpeg8-dev
    $ sudo apt-get install wv libxml2-dev libxslt1-dev libsasl2-dev poppler-utils
    $ sudo apt-get install libdb4.4-dev libldap2-dev
    $ sudo apt-get install git subversion

    $ addgroup --system zope
    $ adduser --system --no-create-home --disabled-login --ingroup zope --disabled-password --shell /bin/false zope

Install Python 2.4. On Ubuntu, use deadsnakes repository. Otherwise build it.

https://launchpad.net/~fkrull/+archive/ubuntu/deadsnakes


Install elevate.cynin
---------------------
::
    $ git clone git@github.com:thet/elevate.cynin.buildout.git

::
    $ python2.4 bootstrap.py -c deploy.cfg  # or dev.cfg
    $ ./bin/buildout -c deploy.cfg  # or dev.cfg


then
----

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
