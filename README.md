Install Zabbix-Agent
=========

This is playbook is responsible by install of the application Zabbix-Agent to O.S CentOS and Ubuntu at versions bellow:

|OS|Version|
|------|---------|
|Ubuntu 18|Bionic|
|Ubuntu 16|Trusty|
|Ubuntu 14|Xenial|
|CentOS|Version 7|
|CentOS|Version 6|
|CentOS|Version 5|


Requirements
------------

This is playbook has necessity of access remote ssh to hosts destination and add the IPs or hostname of the hosts at file *inventory-hosts* witch there is at  project, the IPs separete for *enter*.

Ex inventory-hosts:
```
[hosts-zabbix-agent]
10.0.0.123
serverweb
```

Zabbix-Agent Variables
--------------

The project has variables definitions for S.O and versions at files in directory *vars*, but there is a variable default in file *main.yml* at diretory *default*.

    - vars
      - CentOS-5.yml
      - CentOS-6.yml
      - Ubuntu-trusty.yml
      - Ubuntu-xenial.yml

    - default
      - main.yml


Example of runnig Playbook
----------------

```
$ ansible-playbook -i inventory-hosts play.yml
```
