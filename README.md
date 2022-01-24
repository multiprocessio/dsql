# dsql (WIP): commandline universal database client

dsql is a commandline tool built on top of
[DataStation](https://github.com/multiprocessio/datastation) that
allows you to query any database (supported by DataStation) with a
standard commandline syntax (the SQL you write is still specific to
the database vendor).

## Example

Create a new profile:

```bash
$ dsql --new-profile # or `dsq -n`
Select a vendor:
1. PostgreSQL
2. MySQL
3. SQLite
4. Oracle
5. SQL Server

Pick (1-5): 1

Username: test
Password: ****
Address: localhost
Port:
Profile name: local-postgres

Profile created.
```

Now write a query:

```bash
$ dsql local-postgres "SELECT * FROM users"
```