# simple-ansible-mysql

Hi, this is my simple ansible mysql role. With this role in your playbook you can simply install, configure and manage a mysql/mariadb server.
This role is compatible with the following Linux Distributions:

* Debian (>7)
* Ubuntu (>14.04)
* CentOS (>6.7)

## Configuration / Usage

The role will automatically chose the platform specific install and configuration files. Each platform has its own set of variables set in the vars.yml under the vars section. With the examples included, it will automatically create two database users each with a database assigned (I´ve put this in for a better understanding of the variables/usage of the variables)

### Variable configuration

#### Variables

Below a short description of the used variables and their purpose:

```
mysql_service
```
Name of the database service, platform specific
<br>
<br>

```
mysql_packages
```
List of packages to be installed
<br>
<br>
```
mysql_root: root
```
Name of the database root user / database superuser (when the database server is installed with this role)
<br>
<br>
```
mysql_root_password: SomeSecurePass
```
Password to be set for the root user (when the database server is installed with this role)
<br>
<br>
```
mysql_host: localhost
```
Mysql host
<br>
<br>

```
mysql_user_configuration:
  - user: dbuser01
    database: database01
    password: SecurePass
    collation: utf8_bin
    charset: utf8
```
- user: name of the database user
- database: name of the database to be created
- password: password for the user
- collation: database collation
- charset: database charset

#### Switches
Currently, there are no switches.
