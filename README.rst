How to use this cookiecutter
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
    ├── CHANGELOG.rst
    ├── runtests.py
    ├── src
    │   └── argus_ticket_bugzilla.py
    ├── tests
    │   ├── __init__.py
    │   ├── test_argus_ticket_bugzilla.py
    │   └── test_settings.py
    └── tox.ini

Write your plugin in the file ``src/argus_ticket_bugzilla.py``, your tests in
``tests/test_argus_ticket_bugzilla.py``, your changelog in ``CHANGELOG.rst`` and
most importantly your docs in ``README.rst``.

Your README must explain any extra django settings needed besides the usual
``TICKET_ENDPOINT``, ``TICKET_AUTHENTICATION_SECRET`` and
``TICKET_INFORMATION``.

You should explain how to get what's necessary for authenticating (webhook,
username/password, token, magical email address, ...) and what should be put in
this ticket plugin's ``TICKET_AUTHENTICATION_SECRET``.

Finally, if ``TICKET_INFORMATION`` is at all necessary, you need to describe
(with an example) what should be in it.

Tests can be run with ``tox`` or directly via ``runtests.py``.
