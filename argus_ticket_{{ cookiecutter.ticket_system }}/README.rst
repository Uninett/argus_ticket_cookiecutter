argus_ticket_{{ cookiecutter.ticket_system }}
============={% for _ in cookiecutter.ticket_system %}={% endfor %}

This is a plugin to create tickets in {{ cookiecutter.ticket_system|capitalize }} from
`Argus <https://github.com/Uninett/argus-server>`_

Settings
--------

* ``TICKET_ENDPOINT``: Link to instance, absolute URL
* ``TICKET_AUTHENTICATION_SECRET``: Short explanation

  ::

    {
        "username": username,
        "password": password
    }

* ``TICKET_INFORMATION``: System-specific config

  Remember to jot down what is required and what is optional, if any.

  ::

    {
       "your": "fields",
       "and": "values",
    }

This is also the place to describe any other settings that needs updating in
the Django settings.
