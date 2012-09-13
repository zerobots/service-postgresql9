How to setup PostgreSQL 9
===================

Run the following script, supplying **db**, **db_user**, and **db_password**

```
sudo ansible-playbook -c local deploy.yml -e "db=zerobot_db db_user=zerobot db_password=password"
```

The script above will install PostgreSQL and create your specified database and user.
Once the script it completed, you can login to postgres from any host using:
```
psql -h postgres_server_dns -U zerobot zerobot_db
```