# learn-postgresql-100

|本期版本|上期版本
|:---:|:---:
`Thu Jul 20 21:33:16 CST 2023` | -

## macOS

> `13.4`

```bash
brew install postgresql@15
fish_add_path /usr/local/opt/postgresql@15/bin
```

```
brew services start postgresql@15
```

```bash
psql postgres
```

## Ubuntu

> `22.04`

```bash
ansible-galaxy install -r requirements.yml
```

```bash
sudo su - postgres
psql
```

```bash
sudo systemctl status postgresql@15-main.service
```

```
# cat /var/lib/postgresql/15/main/postmaster.opts
/etc/postgresql/15/main/postgresql.conf

# cat /etc/postgresql/15/main/postgresql.conf|grep pg_hba.conf
/etc/postgresql/15/main/pg_hba.conf
```


## Admin

```
createuser  ${app_name} -P
createdb -O ${app_name} ${app_name}_production -E UTF8 -e
```


## Ref

* <https://www.postgresql.org/>
* [PostgreSQL Apt Repository](https://www.postgresql.org/download/linux/ubuntu/)
* [Community.Postgresql &mdash; Ansible Documentation](https://docs.ansible.com/ansible/latest/collections/community/postgresql/index.html)
* <https://www.pgcli.com/>
* <https://eggerapps.at/postico2/>