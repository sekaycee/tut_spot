# Setup and Use PostgreSQL Database in Termux

Personally I used the commamd `termux-change-repo`.. to select all available mirrors.

## Installation Steps

### `pkg install postgresql`

Install PostgreSQL

### `mkdir ~/.pgsql && initdb ~/.pgsql`

Create skeleton database.
You can change the directory to a custom path.

### `pg_ctl start -D ~/.pgsql`

Start the database server.
You can create an alias (optional).. to shorten the command above.

### `pg_ctl stop -D ~/.pgsql`

Stop the database server.
Optional alias for this command too.
It's also needful.. since You'll probably be running the command often.

### `createuser --superuser --pwprompt username`

Create User.
Replace `username` with yours.

### `createdb dbname`

Create your database.
Again replace dbname with yours

### `psql dbname`

Initiate your database.
Once your database is initialized.. you'll see the prompt `dbname=#`

