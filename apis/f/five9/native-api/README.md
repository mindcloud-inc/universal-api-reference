# Five9: Native API Reference

A consolidated summary of Five9's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://documentation.five9.com/bundle/admin-console/page/admin-console/landing-admin-console.htm
- **API base URL:** `https://api.prod.us.five9.net/acl/v1/`

## Authentication

### Custom

### Credentials

- **password:** `password` · required
- **username:** `username` · required

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
```

[Official authentication documentation](https://documentation.five9.com/bundle/admin-console/page/admin-console/landing-admin-console.htm)

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Campaign Settings](actions/campaign-settings.md) | `GET https://api.prod.us.five9.net/acl/v1/domains/:domainID/permissions/campaignmgmt.ani-settings.view` | [docs](https://documentation.five9.com/bundle/admin-console/page/admin-console/landing-admin-console.htm) |
| [Create User](actions/create-users.md) | `POST https://api.prod.us.five9.net/users/v1/domains/130744/users` | [docs](https://documentation.five9.com/bundle/admin-console/page/admin-console/contact-fields/_ch-contact-fields.htm) |
| [List Users](actions/list-users.md) | `GET https://api.prod.us.five9.net/users/v1/domains/:domainID/users` | [docs](https://documentation.five9.com/bundle/admin-console/page/admin-console/users/_ch-users.htm) |
| [My User Permission's](actions/my-user-permissions.md) | `GET https://api.prod.us.five9.net/acl/v1/domains/130744/my-ui-permissions` | [docs](https://documentation.five9.com/bundle/admin-console/page/admin-console/domain/_ch-user-settings.htm) |
| [Update User](actions/update-user-info.md) | `PATCH https://api.prod.us.five9.net/users/v1/domains/:domainID/users/:userUID` | [docs](https://documentation.five9.com/bundle/admin-console/page/admin-console/users/_ch-users.htm) |
