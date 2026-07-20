# iContact: Native API Reference

A consolidated summary of iContact's API configuration, with links to official documentation.

- **Official docs:** https://help.icontact.com/customers/s/article/API-Developer-Portal
- **API base URL:** `https://app.icontact.com/icp/a/{accountId}/c/{clientFolderId}`

## Authentication

### Custom

### Credentials

- **Account ID:** `accountId` · required · iContact account ID path segment
- **Client Folder ID:** `clientFolderId` · required · iContact client folder ID path segment
- **App ID:** `apiAppId` · required · iContact application ID value
- **Username:** `apiUsername` · required · iContact API username value
- **Password:** `apiPassword` · required · iContact API password value

Send these headers with each API request:

```http
API-AppId: <apiAppId>
API-Password: <apiPassword>
API-Username: <apiUsername>
```

[Official authentication documentation](https://icontact.my.site.com/Help/s/article/Create-and-Manage-API-Keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `API-Version` | `2.2` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; minimum 1). Use `offset` in the query string as the record offset; numbering starts at 0.
