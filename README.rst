PSQL Connect
============

Prompt for one of the databases contained in ``~/.pgpass`` to connect to before launching ``psql``.

See `pgpass <https://www.postgresql.org/docs/9.4/static/libpq-pgpass.html>`_ for more info on how to create a pgpass file.


Installing
----------

.. code-block::

  pip install psql-connect


Creating a standalone executable
--------------------------------

Rather than pollute the system's site-packages, the following will create self contained ``psql-connect`` executable which can then be put on ``PATH``.

.. code-block::

  virtualenv --python=python3 env
  source env/bin/activate
  pip install pex psql-connect
  pex psql-connect -c psql-connect -o psql-connect
  deactivate
  rm -rf env


License
-------

MIT
