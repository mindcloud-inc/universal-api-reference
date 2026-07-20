# Planerka: Native API Reference

A consolidated summary of Planerka's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://help.planerka.app/api
- **OpenAPI specification:** https://planerka.app/rest/doc.json
- **API base URL:** `https://planerka.app/rest/v1`

## Authentication

### API key

Authenticate Planerka REST requests with an API token sent in the x-auth header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-auth: <apiKey>
```

[Official authentication documentation](https://help.planerka.app/api)

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get API status](actions/get-api-status.md) | `GET /` | [docs](https://planerka.app/rest/doc) |
| [List events by date](actions/list-events-by-date.md) | `GET /event/` | [docs](https://planerka.app/rest/doc) |
| [List meeting types](actions/list-meeting-types.md) | `GET /type/` | [docs](https://planerka.app/rest/doc) |
