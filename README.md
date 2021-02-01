## Vagrant LAMP stack provisioning script

A complete Vagrant LAMP stack setup for development based on Ubuntu 20.

### Bootstrap.sh
A shell script that is run by Vagrant on your guest machine. If you need to install any libraries onto the machine during provisioning, add the shell command here. At the moment the script installs the following:
1. apache2
2. PHP 8.0 and PHP 7.4
3. mysql-server
6. git
7. Node
8. composer
9. vim
10. memcached
11. postfix

Boostrap.sh also sets the root password for mysql.
