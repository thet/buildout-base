Django buildout configuration
=============================

Include this files in your buildout:

* etc/base.cfg
* etc/django.cfg

Install
-------
::
    $ python-2.6 bootrap.py -d
    $ ./bin/buildout

Create the DB
-------------
::
    $ ./bin/django syncdb

Import the data fixtures
------------------------
::
    $ ./bin/django loaddata musicfocus $ ./bin/django loaddata broadcastformats $ ./bin/django loaddata rrules $ ./bin/django loaddata showinformation $ ./bin/django loaddata showtopics $ ./bin/django loaddata hosts $ ./bin/django loaddata shows

Run the server
--------------
::
    $ ./bin/django runserver
