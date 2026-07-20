# Oracle DB Legacy: Native API Reference

A consolidated summary of Oracle DB Legacy's API configuration, with links to official documentation.

- **Official docs:** https://docs.oracle.com/cd/B19306_01/server.102/b14200/toc.htm
- **API base URL:** `https://www.oracle.com/database/`

## Authentication

### Oracle DB Legacy connection

### Credentials

- **Host:** `host` · required
- **Port:** `port` · optional
- **Username:** `username` · required
- **Password:** `password` · required
- **SID:** `sid` · optional · Use this only when your Oracle connection string ends with host:port:SID.
- **Service Name:** `serviceName` · optional · Use this only when your Oracle connection string uses //host:port/service_name.
- **Timeout:** `timeout` · optional · Optional timeout in milliseconds for the Oracle connection and query.

Pass these values to the database driver when opening the connection. This is a driver connection rather than HTTP authentication, so there is no `Authorization` header.

[Official authentication documentation](https://docs.oracle.com/cd/B19306_01/java.102/b14355/urls.htm)
