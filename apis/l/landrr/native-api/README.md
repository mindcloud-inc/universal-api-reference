# Landrr: Native API Reference

A consolidated summary of Landrr's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://landrrapp.io/api/documentation/
- **API base URL:** `https://api.landrrapp.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.getlandrr.com/article/467-find-your-landrr-account-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | `GET /api/getCampaigns` | [docs](https://landrrapp.io/api/documentation/) |
| [List Leads](actions/list-leads.md) | `GET /api/getEmailLeadsFromapi` | [docs](https://landrrapp.io/api/documentation/) |
| [Verify API Key](actions/verify-api-key.md) | `GET /api/auth` | [docs](https://landrrapp.io/api/documentation/) |
