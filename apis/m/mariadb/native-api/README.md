# MariaDB: Native API Reference

A consolidated summary of MariaDB's API configuration, with links to official documentation.

- **Official docs:** https://mariadb.com/docs/server

## Authentication

### MariaDB connection

### Credentials

- **Host:** `host` · required
- **Port:** `port` · optional
- **Database:** `database` · required
- **User:** `user` · required
- **Password:** `password` · optional

Pass these values to the database driver when opening the connection. This is a driver connection rather than HTTP authentication, so there is no `Authorization` header.

[Official authentication documentation](https://mariadb.com/docs/server/mariadb-quickstart-guides/mariadb-connecting-guide)
