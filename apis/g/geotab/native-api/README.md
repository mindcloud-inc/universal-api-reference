# Geotab: Native API Reference

A consolidated summary of Geotab's API configuration, with links to official documentation.

- **Official docs:** https://developers.geotab.com/myGeotab/introduction/
- **API base URL:** `https://{server}/apiv1`

## Authentication

### MyGeotab

Connect with a MyGeotab database user.

### Credentials

- **Server:** `server` · required · The MyGeotab server hostname. Use my.geotab.com unless authentication returns a different server path.
- **Database:** `database` · required · The MyGeotab database name.
- **Username:** `userName` · required · The username, typically an email address, for the MyGeotab API user.
- **Password:** `password` · required · The password for the MyGeotab API user.

[Official authentication documentation](https://developers.geotab.com/myGeotab/guides/concepts/index.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
