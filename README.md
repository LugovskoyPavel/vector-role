Role Name
=========

Instal_vector

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

| Vars	| Description	 | Value | Location |
| ------------- |:------------------:|:------------------:|:-------------------:|
| vector_version |	Vector version to install |	0.22.1 |	defaults/main.yml |
| vector_clickhouse_ip |	Addres of Clickhouse instance |	localhost |	defaults/main.yml |
| clickhouse_db_name |	Clickhouse DB where to store logs |	"logs" |	defaults/main.yml |
| clickhouse_table_name |	Clickhouse table name to write logs	| "data_logs" |	defaults/main.yml |
| vector_url |	URL for Vector download |	https://packages.timber.io/vector/{{ vector_version }}/vector-{{ vector_version }}-1.x86_64.rpm	vars/main.yml |
| vector_config_dir |	Vector config file location	"/etc/vector" |	vars/main.yml |
| vector_config |	Vector config file |	value below	default/main.yml |


Example Playbook
----------------
```
- name: Install Vector
  hosts: vector1 
  role:
    -vector 
```

License
-------

BSD

Author Information
------------------

Lugovskoy Pavel
