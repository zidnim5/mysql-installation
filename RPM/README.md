
<p align="right">
<a href="#">  
<img src="https://shields.io/badge/MySQL-lightgrey?logo=mysql&style=for-the-badge&logoColor=white&labelColor=blue" />
</a>
</p>

<br/>

# MySQL Installation


This repository is published in order to share how to Install MySQL database using RPM.
The official documentation can be found at <a href="https://dev.mysql.com/doc/refman/8.0/en/installing.html"> dev.mysql.com </a>



## Download & Install RPM Installer

Please download the file from official website https://dev.mysql.com/downloads/mysql/.

1. `mysql-common`
2. `mysql-client`
3. `mysql-client-plugin`
4. `mysql-libs`
5. `mysql-icu`
6. `mysql-server`

</br>
To install using this command :

```
rpm -ivh name_file.rpm
```

</br>
Makesure MySQL installation using this command :

```
mysql -V
```

## Example Configuration File

Configuration file is located in /etc/my.cnf

```
[mysqld@database_satu]
datadir=/var/lib/mysql/database_satu
socket=/var/lib/mysql/database_satu/mysql.sock
port=3308
log-error=/var/lib/mysql/database_satu/database_satu.log

[mysqld@database_dua]
datadir=/var/lib/mysql/database_dua
socket=/var/lib/mysql/database_dua/dua.sock
port=3309
log-error=/var/lib/mysql/database_dua/database_dua.log
```


## Managing MySQL Server with systemd

Systemd provides automatic MySQL server startup and shutdown. It also enables manual server management using the systemctl command.


```
systemctl {start|stop|restart|status} mysqld@database_satu
```

<br/>

## References

https://dev.mysql.com/doc/refman/8.0/en/installing.html

http://www.pervasivecode.com/blog/2008/03/29/making-selinux-allow-a-nonstandard-mysql-port-number-on-centos-51



