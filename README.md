# postgresql 9.4 script for Centos 7x64

For use on a clean CentOS 7.x64 box only.

This script installs:

- postgresql94 

- postgresql94-devel

- postgresql94-server 

- postgresql94-libs 

- postgresql94-contrib 

- postgresql94-plperl 

- postgresql94-plpython 

- postgresql94-pltcl 

- postgresql94-python 

- postgresql94-odbc 

- postgresql94-jdbc 

- perl-DBD-Pg 

- pgbouncer

- Webmin

- IP tables

The script also creates the following:

- A minimally privilaged user (pgadmin)

- Disables root log in

- Sets IP tables

- Configures Webmin for managing PostgreSQL

- Installs a self-signed SSL

- Updates pga_hba.conf to MD5 and SSL

- Updates postgresql.conf for SSL.

- You can change the SSH port as well as the user name to whatever you like.  You can also add/remove packages.

- Once completed, it will display the new passwords for pgadmin, root, postgres, and ssl as well as write them to an auth.txt file.  It will also restart SSHD, so be sure to copy new password!

-This script does NOT install IP tables. For IP Tables, please use the CentOS 6 script  (https://github.com/brainfurnace/postgresql-9.4-script-centos-6x64) or install your own FirewallD or IPTables. 


Example:

Passwords saved in /root/auth.txt

pg pass: DqVnavTlCXcSKfgprgUtjF-20rpfsKui

ssl pass: yxaQJCXgueTw19XEOMPdZzNd5n6rwVOG

pgadmin pass: A0RUHtEfSFC82mHeDP_ixrRavk7itgkE

root pass: RvZEHkZv-AeQS-ce0Mcnif7GxmmJ-zxN
