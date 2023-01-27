pgbackup
========


Python CLI for backup remote PostgreSQL database either locally or to AWS S3

Preparing the Devlopment
------------------------

1. Ensure ``pip`` and ``pipenv`` are installed.
2. Clone repository: ``git clone git@github.com:example/pgbackup``.
3. ``cd`` into the repository.
4. Fetch development dependencies ``make install``.
5. Activate virtualenv: ``pipenv shell``.


Usage
-----

Pass in a full database connection string URL, the storage driver and the destination

S3 Example w/ bucket name:

::
        $ pgbackup postgres://user:pass@db-ip:port/db-name --driver s3 backups
Local Example w/ local path:

:: 
        $ pgbackup postgres://user:pass@db-ip:port/db-name --driver local /var/local/db_one/backups/dump.sql

Running Tests
-------------

Run test locally using ``make`` if virtualevn is active

::
        $ make

If virtualenv is not active

::

        $ pipenv run make


