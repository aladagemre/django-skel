django-skel
===========

An extension to [django-skel](https://github.com/rdegges/django-skel) of rdegges. See http://django-skel.rtfd.org/ for original
django-skel documentation.

Django-skell provides you a django project template (skeleton) so that you can quickly start coding without
much configuration and deploy your code to Heroku easily.

This extension provides:

    * A mainpage with Bootstrap 3.0.2
    * Social authorization mechanism with django-allauth

This way, you can eliminate the time wasted for HTML templates, authorization integration etc.

How to use it?
=================

    $ curl https://raw.github.com/aladagemre/django-skel/master/install.py|python

Then follow the wizard, give the project name and specify heroku settings.

When the downloads and automatic configurations are done, you've got a clean project.
Firefox should open a new tab and display the admin panel to you.

Social Settings
=================

In the admin panel's Social App models, create new objects for each system (Facebook, Twitter, Google, Github etc).
If you want to add other social login systems, add to AUTH_APPS of settings/common.py. See django-allauth for
possible login systems.

If you don't want to use them, you can remove the appropriate HTML codes from the index page.


Deploying
============

When you want to deploy on Heroku,

    $ git push heroku master
    $ heroku run python manage.py syncdb
    $ heroku run python manage.py migrate
    $ heroku run python manage.py collectstatic

And perform similar social app settings on Heroku server.
