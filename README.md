# -Insecure-admin-access-and-Information-Disclosure

vulnerability name :  Insecure admin access and Information Disclosure

Severity : CWE-205, ISO27001-A.14.2.5, WASC-13, OWASP 2017-A6

vulnerable URL : https://mysql.server.cloudya.net/index.php

Description:

phpMyAdmin is an application written in the PHP language that provides a web-based interface for the administration of MySQL databases. The initial MySQL root account password is empty, so anyone can connect to the MySQL server as root, without a password and be granted all privileges.

Summary :

phpMyAdmin is a tool that performs the basic MySQL operations such as creating, altering, and dropping databases, tables, fields, indexes, and users. It can execute SQL statements and manage relations between objects. It also provides a rich web interface, a SQL parser and many other features. It is one of the most popular database management tools on the web.

phpMyAdmin is internal with inadequate access control and authentication mechanisms required for public access applications. It relies on username/password authentication without support for 2FA, and as a result, it is an easy target for attackers.

Impact :
Attackers can leverage compromised credentials or brute force attacks to log into the phpMyAdmin interface to obtain full read-write access to sensitive data.

Solution :
Remove phpMyAdmin or ensure reverse proxies protect it backed by strong authentication.

Reference :

https://hackerone.com/reports/297339
