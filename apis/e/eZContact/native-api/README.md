# EZContact: Native API Reference

A consolidated summary of EZContact's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://ezcontact.ai/en/integraciones/
- **API base URL:** `https://app.ezcontact.ai/api`

## Authentication

### API Key

Authenticate with the EZContact API key generated in API / Integraciones.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://app.ezcontact.ai/docs/API.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Search Contacts](actions/search-contacts.md) | `POST /mcp.php` | [docs](https://app.ezcontact.ai/docs/API.md) |
