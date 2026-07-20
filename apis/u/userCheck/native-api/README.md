# UserCheck: Native API Reference

A consolidated summary of UserCheck's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://www.usercheck.com/docs/api/introduction
- **API base URL:** `https://api.usercheck.com`

## Authentication

### API Key

Authenticate with a UserCheck API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.usercheck.com/docs/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Domain to Blocklist](actions/add-domain-to-blocklist.md) | `POST /blocklist` | [docs](https://www.usercheck.com/docs/api/blocklist-endpoint) |
| [Bulk Add Domains to Blocklist](actions/bulk-add-domains-to-blocklist.md) | `POST /blocklist/bulk` | [docs](https://www.usercheck.com/docs/api/blocklist-endpoint) |
| [Evaluate Gate Decision](actions/evaluate-gate-decision.md) | `POST /v0/gates/:gateId/decisions` | [docs](https://www.usercheck.com/docs/gates/decision-endpoint) |
| [Get Blocklisted Domain](actions/get-blocklisted-domain.md) | `GET /blocklist/:domain` | [docs](https://www.usercheck.com/docs/api/blocklist-endpoint) |
| [Get Status](actions/get-status.md) | `GET /status` | [docs](https://www.usercheck.com/docs/api/status-endpoint) |
| [List Blocklisted Domains](actions/list-blocklisted-domains.md) | `GET /blocklist` | [docs](https://www.usercheck.com/docs/api/blocklist-endpoint) |
| [Remove Domain from Blocklist](actions/remove-domain-from-blocklist.md) | `DELETE /blocklist/:domain` | [docs](https://www.usercheck.com/docs/api/blocklist-endpoint) |
| [Validate Domain](actions/validate-domain.md) | `GET /domain/:domain` | [docs](https://www.usercheck.com/docs/api/domain-endpoint) |
| [Validate Email](actions/validate-email.md) | `GET /email/:email` | [docs](https://www.usercheck.com/docs/api/email-endpoint) |
