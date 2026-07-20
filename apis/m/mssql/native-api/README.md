# Microsoft SQL: Native API Reference

A consolidated summary of Microsoft SQL's API configuration, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/sql/

## Authentication

### Microsoft SQL connection

### Credentials

- **Server:** `server` · required
- **Port:** `port` · optional
- **Database:** `database` · required
- **Username:** `username` · required
- **Password:** `password` · optional
- **Encryption:** `encrypt` · optional
- **Timeout:** `timeout` · optional
- **Use ODBC:** `odbc` · optional

Pass these values to the database driver when opening the connection. This is a driver connection rather than HTTP authentication, so there is no `Authorization` header.

[Official authentication documentation](https://learn.microsoft.com/en-us/ssms/f1-help/connect-to-server-login-page-database-engine)
