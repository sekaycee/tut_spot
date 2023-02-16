# Setup and Use PostgreSQL Database in Termux

Personally I used the commamd `termux-change-repo`.. to select all available mirrors.

## Installation Steps

1. Install PostgreSQL

```
$ pkg install postgresql
```

2. Create skeleton database

```
$ mkdir ~/.pgsql
$ initdb ~/.pgsql
```
You can change the directory to whatever path you want

3. Start the database server

```
$ pg_ctl start -D ~/.pgsql
```
I created an alias (optional).. to shorten the command above.

4. Stop the database server

```
$ pg_ctl stop -D ~/.pgsql
```
Optional alias for this command too.
It's also needful since I'll running the command often.

5. Create User

```
$ createuser --superuser --pwprompt username
```
Replace `username` with yours

6. Create your database

```
$ createdb dbname
```
Again replace dbname with yours

7. Initiate your database

```
$ psql dbname
```

8. Once your database is initialized.. you'll see the prompt

```
dbname=#
```

