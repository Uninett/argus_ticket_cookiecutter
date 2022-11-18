How to use this cokkiecutter
============================

If you do not have cookiecutter you will have to install it.

Then, run::

    cookiecutter argus_ticket_cookiecutter

It will ask you for two things:

1. A snake case name for your ticket system
2. Your dependencies. If more than one, separate them with a comma

For example:

If you answered "bugzilla" for ``ticket_system`` a directory is created that is
called ``argus_ticket_bugzilla``.

Here's the generated directory tree inside ``argus_ticket_bugzilla``::

    ├── LICENSE
    ├── Makefile
    ├── pyproject.toml
    ├── README.rst
    ├── runtests.py
    ├── src
    │   └── argus_ticket_bugzilla.py
    ├── tests
    │   ├── __init__.py
    │   ├── test_argus_ticket_bugzilla.py
    │   └── test_settings.py
    └── tox.ini

Write your plugin in the file ``src/argus_ticket_bugzilla.py``, your tests in
``tests/test_argus_ticket_bugzilla.py``, your changelog in ``CHANGELOG.md and
most importantly your docs in ``README.rst``.

Your README must explain any extra django settings needed besides the usual
``TICKET_PLUGIN``, ``TICKET_AUTHENTICATION`` and ``TICKET_INFORMATION``.

You should explain how to get what's necessary for authenticating (webhook?
username/password? magical email address?) and what should be put in this
ticket plugin's ``TICKET_AUTHENTICATION``.

Finally, if ``TICKET_INFORMATION`` is at all necessary, you need to describe
(with an example) what should be in it.

Tests can be run with ``tox`` or directly via ``runtests.py``.
