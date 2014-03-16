Installation
---
    $ git clone git@github.com:MartijnBraam/cms-dev-deploy.git
    $ ln -s path/to/cms-dev-deploy/makedev /usr/local/sbin
    $ cp cms-dev-deploy/example.dev.cnf ~/.dev.cnf

Configuration
---
Edit the parameters in ~/.dev.cnf to match your environment.

Parameter   | Description
----------- | ------------
webroot     | Path in which to create the cms installations
mysqluser   | Username for mysql account. needs permission to create databases
mysqlpass   | Password for mysql account
adminuser   | Username for administrative user in new cms installations
adminpass   | Password for administrative user
vhostfile   | New apache vhosts wil be appended to this file
apacheuser  | User apache is configured to run as. Used to set permissions on cms directory
permgroup   | Primary group of your user account. Used to make sure you can edit all cms files

Usage
---

    $ sudo makedev example
This command wil add the hostname "example.dev" to /etc/hosts, create an apache vhost and ask you which cms you want to install.

