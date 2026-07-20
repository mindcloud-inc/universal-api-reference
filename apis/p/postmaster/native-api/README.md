# Postmaster+: Native API Reference

A consolidated summary of Postmaster+'s API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://postmasterplus.app/docs
- **OpenAPI specification:** https://postmasterplus.app/docs.openapi
- **API base URL:** `https://postmasterplus.app`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://postmasterplus.app/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 15; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Single Email](actions/delete-single-email.md) | `DELETE /api/v1/intelligence/single-emails/:email` | [docs](https://postmasterplus.app/docs) |
| [Get Screenshot](actions/get-screenshot.md) | `GET /api/v1/screenshot/:id` | [docs](https://postmasterplus.app/docs) |
| [List Screenshots](actions/list-screenshots.md) | `GET /api/v1/screenshots` | [docs](https://postmasterplus.app/docs) |
| [Retrieve Blocklist Scan Status](actions/retrieve-blocklist-scan-status.md) | `GET /api/v1/blocklist/scan/status/:id` | [docs](https://postmasterplus.app/docs) |
| [Retrieve Domain](actions/retrieve-domain.md) | `GET /api/v1/domains/:id` | [docs](https://postmasterplus.app/docs) |
| [Retrieve Domain Feed](actions/retrieve-domain-feed.md) | `GET /api/v1/domains/:id/feed` | [docs](https://postmasterplus.app/docs) |
| [Retrieve Domains](actions/retrieve-domains.md) | `GET /api/v1/domains` | [docs](https://postmasterplus.app/docs) |
| [Retrieve IPs](actions/retrieve-i-ps.md) | `GET /api/v1/ips` | [docs](https://postmasterplus.app/docs) |
| [Retrieve IP](actions/retrieve-ip.md) | `GET /api/v1/ips/:id` | [docs](https://postmasterplus.app/docs) |
| [Retrieve IP Feed](actions/retrieve-ip-feed.md) | `GET /api/v1/ips/:id/feed` | [docs](https://postmasterplus.app/docs) |
| [Retrieve Single Email](actions/retrieve-single-email.md) | `GET /api/v1/intelligence/single-emails/:email` | [docs](https://postmasterplus.app/docs) |
| [Scan Single Email](actions/scan-single-email.md) | `POST /api/v1/intelligence/single-emails/scan` | [docs](https://postmasterplus.app/docs) |
| [Start Blocklist Scan](actions/start-blocklist-scan.md) | `POST /api/v1/blocklist/scan/start` | [docs](https://postmasterplus.app/docs) |
| [Take Screenshot](actions/take-screenshot.md) | `POST /api/v1/screenshot/take` | [docs](https://postmasterplus.app/docs) |
