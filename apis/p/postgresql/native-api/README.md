# PostgreSQL: Native API Reference

A consolidated summary of PostgreSQL's API configuration, with links to official documentation.

- **Official docs:** https://www.postgresql.org/docs/current/index.html

## Authentication

### PostgreSQL connection

### Credentials

- **Host:** `host` · required
- **Port:** `port` · optional
- **Database:** `database` · required
- **User:** `user` · required
- **Password:** `password` · optional
- **SSL:** `ssl` · optional
- **Certificate:** `certificate` · optional
- **Reject Unauthorized:** `rejectUnauthorized` · optional
- **Timeout:** `timeout` · optional
- **Use ODBC:** `odbc` · optional

Pass these values to the database driver when opening the connection. This is a driver connection rather than HTTP authentication, so there is no `Authorization` header.

[Official authentication documentation](https://www.postgresql.org/docs/current/libpq-connect.html)
