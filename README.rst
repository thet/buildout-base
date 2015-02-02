buildout-base
=============

Generic zc.buildout base config files, which can be used by different projects,
at least by me. Currently very Zope/Plone based, but support for Django or the
like will likely come.

TODO
----

- Make individual configs usable standalone.

- etc/deliverance.cfg
    - deliverance-init: path to input file not accessible when refering via http
    - rules-file is project specific.

Notes on Plone < 4
------------------

Plone 2.x and 3 need Python 2.4 to run. To install python 2.4 with the
requirements, you need for Plone < 4, you can do the following:

$ git clone git@github.com:bluedynamics/bda-naked-python.git python24
$ cd python24
$ python bootstrap.py -c buildout2.4.cfg
$ ./bin/buildout -c buildout2.4.cfg

$ hg clone https://thet@bitbucket.org/tarek/distribute
$ hg up 0.6-maintenance
$ ./bin/python24 distribute_setup.py

$ ./parts/python24/bin/easy_install zc.buildout==1.4.4

Then, run in your Plone < 4 buildout:

$ PATH_TO/bin/python24 bootstrap.py --distribute -c BUILDOUT.cfg
$ ./bin/buildout -c BUILDOUT.cfg



Author
------
Johannes Raggam, BlueDynamics Alliance, <raggam-nl@adm.at>
