# SqlBak: Native API Reference

A consolidated summary of SqlBak's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://sqlbak.docs.apiary.io/
- **OpenAPI specification:** https://sqlbak.docs.apiary.io/api-description-document
- **API base URL:** `https://sqlbak.com/public-api/v1`

## Authentication

### API Token

### Credentials

- **API Key:** `apiKey` · required
- **Install Secret Key:** `installSecretKey` · optional · Registers a SqlBak app/server with your SqlBak account.

Send these headers with each API request:

```http
X-SqlBak-Token: <apiKey>
```

[Official authentication documentation](https://sqlbak.com/blog/building-automated-backup-monitoring-with-the-sqlbak-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The current page number is read from `page`.

## Pagination

Use `page_size` in the query string to set the page size (default 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account Information](actions/get-account-information.md) | `GET /me` | [docs](https://sqlbak.docs.apiary.io/) |
| [List DBMS Connections](actions/list-dbms-connections.md) | `GET /dbms_connections` | [docs](https://sqlbak.docs.apiary.io/) |
| [List Destinations](actions/list-destinations.md) | `GET /destinations` | [docs](https://sqlbak.docs.apiary.io/) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://sqlbak.docs.apiary.io/) |
| [List Servers](actions/list-servers.md) | `GET /servers` | [docs](https://sqlbak.docs.apiary.io/) |
