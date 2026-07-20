# PageX: Native API Reference

A consolidated summary of PageX's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://rapidapi.com/thunderhurt/api/pagexcrm
- **API base URL:** `https://www.pagexcrm.com`

## Authentication

### API Key

Use a PageX API key from the Integrations > API page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.pagexcrm.com/plugins/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Lead](actions/add-lead.md) | `POST /api/lead` | [docs](https://rapidapi.com/thunderhurt/api/pagexcrm) |
