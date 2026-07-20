# Powrbot: Native API Reference

A consolidated summary of Powrbot's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://powrbot.com/cpages/docs/
- **API base URL:** `https://powrbot.com/api/v1`

## Authentication

### Secret Key

Authenticate with a Powrbot developer secret key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://powrbot.com/cpages/docs/)

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Download Search CSV](actions/download-search-csv.md) | `GET /search/:searchId/download/` | [docs](https://powrbot.com/cpages/docs/) |
| [Get Search](actions/get-search.md) | `GET /search/:searchId/` | [docs](https://powrbot.com/cpages/docs/) |
| [List Searches](actions/list-searches.md) | `GET /search/` | [docs](https://powrbot.com/cpages/docs/) |
| [Search Company](actions/search-company.md) | `GET /search/single/` | [docs](https://powrbot.com/cpages/docs/) |
| [Start Bulk Search](actions/start-bulk-search.md) | `POST /search/` | [docs](https://powrbot.com/cpages/docs/) |
