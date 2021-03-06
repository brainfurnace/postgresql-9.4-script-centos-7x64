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

- A minimally privilaged user (pgadmin - change to whatever you like)

- Disables root log in

- Resets the root password to a 32 character string

- Sets IP tables

- Configures Webmin for managing PostgreSQL

- Installs a self-signed SSL

- Updates pga_hba.conf to MD5 and SSL

- Updates postgresql.conf for SSL.

- You can change the SSH port as well as the user name to whatever you like.  You can also add/remove packages.

- Once completed, it will display the new passwords for pgadmin, root, postgres, and ssl as well as write them to an auth.txt file.  It will also restart SSHD, so be sure to copy new password!

-This script uses IP Tables and not firewalld. If you want to set up firewalld, comment out the iptable lines as noted.

Usage: 

1. Download the script to a clean CentOS 7.x64 box or use wget <code>wget https://github.com/DavidGhedini/postgresql-9.4-script-centos-7x64/blob/master/pgsql-9.4-centos-7x-64.sh</code>
2. Make it executable <code> chmod 755 pgsql-9.4-centos-7x-64.sh</code>
3. Execute it <code>./pgsql-9.4-centos-7x-64.sh</code>


Example Output at end of script:

Passwords saved in /root/auth.txt

pg pass: DqVnavTlCXcSKfgprgUtjF-20rpfsKui

ssl pass: yxaQJCXgueTw19XEOMPdZzNd5n6rwVOG

pgadmin pass: A0RUHtEfSFC82mHeDP_ixrRavk7itgkE

root pass: RvZEHkZv-AeQS-ce0Mcnif7GxmmJ-zxN
