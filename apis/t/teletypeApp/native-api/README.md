# Teletype App: Native API Reference

A consolidated summary of Teletype App's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://teletype.app/help/api/
- **API base URL:** `https://api.teletype.app/public/api/v1`

## Authentication

### API Key

Teletype Public API uses a project-scoped token. MindCloud should send the raw token in the X-Auth-Token header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Auth-Token: <apiKey>
```

[Official authentication documentation](https://teletype.app/help/api/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 25; minimum 1). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Message Template Catalog](actions/get-message-template-catalog.md) | `GET /template-message/list` | [docs](https://teletype.app/help/api/) |
| [Get Project API Status](actions/get-project-api-status.md) | `GET /project/api-status` | [docs](https://teletype.app/help/api/) |
| [Get Project Balance](actions/get-project-balance.md) | `GET /project/balance` | [docs](https://teletype.app/help/api/) |
| [Get Project Details](actions/get-project-details.md) | `GET /project/details` | [docs](https://teletype.app/help/api/) |
| [Get Project Operators](actions/get-project-operators.md) | `GET /project/operators` | [docs](https://teletype.app/help/api/) |
| [Get Project Tariff](actions/get-project-tariff.md) | `GET /project/tariff` | [docs](https://teletype.app/help/api/) |
| [List Appeal Categories](actions/list-appeal-categories.md) | `GET /appeal-categories/list` | [docs](https://teletype.app/help/api/) |
| [List Channels](actions/list-channels.md) | `GET /channels` | [docs](https://teletype.app/help/api/) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://teletype.app/help/api/) |
| [List Dialogs](actions/list-dialogs.md) | `GET /dialogs` | [docs](https://teletype.app/help/api/) |
| [List Messages](actions/list-messages.md) | `GET /messages` | [docs](https://teletype.app/help/api/) |
| [List Tags](actions/list-tags.md) | `GET /tag/list` | [docs](https://teletype.app/help/api/) |
| [List Template Directories](actions/list-template-directories.md) | `GET /template-message/directories` | [docs](https://teletype.app/help/api/) |
| [Update Public API Settings](actions/update-public-api-settings.md) | `POST /project/update-public-api` | [docs](https://teletype.app/help/api/) |
