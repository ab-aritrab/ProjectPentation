LINKS for Add 18.04 repo to Ubuntu 20.04 

https://askubuntu.com/questions/1261614/ubuntu-20-04-libssl-so-1-0-0-cannot-open-shared-object-file-no-such-file-or-d

LINK for Latest SQL server 

https://docs.microsoft.com/en-us/troubleshoot/sql/general/determine-version-edition-update-level

https://docs.microsoft.com/en-US/troubleshoot/sql/general/determine-version-edition-update-level#sql-server-2012

https://docs.microsoft.com/en-us/sql/connect/odbc/linux-mac/installing-the-microsoft-odbc-driver-for-sql-server?view=sql-server-2017

LINKS for SQLserevr-2017

https://docs.microsoft.com/en-us/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-ver15

https://docs.microsoft.com/en-us/sql/linux/sql-server-linux-setup?view=sql-server-ver15#offline

https://docs.microsoft.com/en-us/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-2017&preserve-view=true

https://docs.microsoft.com/en-us/sql/linux/quickstart-install-connect-ubuntu?view=sql-server-2017&preserve-view=true

https://docs.microsoft.com/en-us/sql/linux/sql-server-linux-release-notes?view=sql-server-ver15

***https://packages.microsoft.com/ubuntu/16.04/mssql-server-2017/pool/main/m/mssql-server/***

GUI LINUX (SAME LIKE SSMS)

https://askubuntu.com/questions/788197/graphical-ms-sql-clients-for-a-ubuntu-desktop

```
sudo dpkg -i mssql-server_14.0.3391.2-12_amd64.deb
"-------OUTPUT---------"
Selecting previously unselected package mssql-server.
(Reading database ... 177874 files and directories currently installed.)
Preparing to unpack mssql-server_14.0.3391.2-12_amd64.deb ...
Unpacking mssql-server (14.0.3391.2-12) ...
dpkg: dependency problems prevent configuration of mssql-server:
 mssql-server depends on libjemalloc1; however:
  Package libjemalloc1 is not installed.
 mssql-server depends on libc++1; however:
  Package libc++1 is not installed.
 mssql-server depends on libssl1.0.0; however:
  Package libssl1.0.0 is not installed.
 mssql-server depends on python (>= 2.7.0); however:
  Package python is not installed.
 mssql-server depends on libsss-nss-idmap0; however:
  Package libsss-nss-idmap0 is not installed.
 mssql-server depends on gawk; however:
  Package gawk is not installed.
 mssql-server depends on libsasl2-modules-gssapi-mit; however:
  Package libsasl2-modules-gssapi-mit is not installed.

dpkg: error processing package mssql-server (--install):
 dependency problems - leaving unconfigured
Processing triggers for libc-bin (2.31-0ubuntu9.7) ...
Processing triggers for man-db (2.9.1-1) ...
Errors were encountered while processing:
"-------OUTPUT-END--------"

sudo apt --fix-broken install
sudo apt install libjemalloc1
sudo apt install libc++1
sudo apt install libssl1.0.0
sudo apt install libsss-nss-idmap0
sudo apt install gawk
sudo apt install libsasl2-modules-gssapi-mit
wget https://repo.percona.com/apt/pool/main/j/jemalloc/libjemalloc1_3.6.0-2.focal_amd64.deb
sudo dpkg -i libjemalloc1_3.6.0-2.focal_amd64.deb 
sudo nano /etc/apt/sources.list  
	"ADD: deb http://security.ubuntu.com/ubuntu xenial-security main" //at the end of lines
sudo apt update
sudo apt install libssl1.0.0
sudo apt install libjemalloc1
sudo dpkg -i mssql-server_14.0.3391.2-12_amd64.deb 
python -V
wget http://archive.ubuntu.com/ubuntu/pool/universe/p/python2.7/python2.7_2.7.18-1~20.04.1_amd64.deb
sudo dpkg -i python2.7_2.7.18-1~20.04.1_amd64.deb 
sudo apt install python2.7
sudo apt --fix-broken install

======================================
sudo dpkg -i mssql-server_14.0.3391.2-12_amd64.deb 

"-----OUTPUT---------"
(Reading database ... 178991 files and directories currently installed.)
Preparing to unpack mssql-server_14.0.3391.2-12_amd64.deb ...
Unpacking mssql-server (14.0.3391.2-12) over (14.0.3391.2-12) ...
Setting up mssql-server (14.0.3391.2-12) ...
Locale en_IN not supported. Using en_US.

+--------------------------------------------------------------+
Please run 'sudo /opt/mssql/bin/mssql-conf setup'
to complete the setup of Microsoft SQL Server
+--------------------------------------------------------------+

Processing triggers for libc-bin (2.31-0ubuntu9.7) ...
Processing triggers for man-db (2.9.1-1) ...

"-----------------------"

```

