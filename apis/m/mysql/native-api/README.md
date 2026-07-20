# MySQL: Native API Reference

A consolidated summary of MySQL's API configuration, with links to official documentation.

- **Official docs:** https://dev.mysql.com/doc/refman/8.4/en/

## Authentication

### MySQL connection

### Credentials

- **Host:** `host` · required
- **Port:** `port` · optional
- **Database:** `database` · required
- **User:** `user` · required
- **Password:** `password` · optional
- **Timeout:** `timeout` · optional
- **Use ODBC:** `odbc` · optional

Pass these values to the database driver when opening the connection. This is a driver connection rather than HTTP authentication, so there is no `Authorization` header.

[Official authentication documentation](https://dev.mysql.com/doc/refman/8.4/en/connecting.html)
