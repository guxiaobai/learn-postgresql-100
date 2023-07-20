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
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -

apt-get update
apt-get install -y postgresql-15 postgresql-client-15 libpq-dev

```

```bash
sudo systemctl status postgresql@15-main.service
```

```bash
sudo su - postgres
psql
```

* `/etc/postgresql/15/main/postgresql.conf`



## Ref

* <https://www.postgresql.org/>
* [PostgreSQL Apt Repository](https://www.postgresql.org/download/linux/ubuntu/)