# Azure SQL: Native API Reference

A consolidated summary of Azure SQL's API configuration, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/azure/azure-sql/

## Authentication

### Azure SQL connection

### Credentials

- **Server:** `server` · required
- **Port:** `port` · optional
- **Database:** `database` · required
- **Username:** `username` · optional
- **Password:** `password` · optional
- **Client Id:** `clientId` · optional
- **Client Secret:** `clientSecret` · optional · Required only for Azure Active Directory Service Principal Secret authentication type
- **Tenant Id:** `tenantId` · optional
- **Timeout:** `timeout` · optional
- **Encrypt:** `encrypt` · optional
- **Use ODBC:** `odbc` · optional
- **Authentication Type:** `authenticationType` · optional

Pass these values to the database driver when opening the connection. This is a driver connection rather than HTTP authentication, so there is no `Authorization` header.

[Official authentication documentation](https://learn.microsoft.com/en-us/fabric/data-factory/connector-azure-sql-database)
