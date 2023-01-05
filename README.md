Role Name
=========

Instal_vector

Role Variables
--------------

| Vars	| Description	 | Value | Location |
| ------------- |:------------------:|:------------------:|:-------------------:|
| vector_version |	Vector version to install |	0.22.1 |	defaults/main.yml |
| vector_clickhouse_ip |	Addres of Clickhouse instance |	localhost |	defaults/main.yml |
| clickhouse_db_name |	Clickhouse DB where to store logs |	"logs" |	defaults/main.yml |
| clickhouse_table_name |	Clickhouse table name to write logs	| "data_logs" |	defaults/main.yml |
| vector_url |	URL for Vector download |	https://packages.timber.io/vector/{{ vector_version }}/vector-{{ vector_version }}-1.x86_64.rpm |	defaults/main.yml |
| vector_config_dir |	Vector config file location |	"/etc/vector" |	defaults/main.yml |
| vector_config |	Vector config file |	value below |	default/main.yml |


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
