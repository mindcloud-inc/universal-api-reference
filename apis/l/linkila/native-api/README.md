# Linkila: Native API Reference

A consolidated summary of Linkila's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://app.linkila.com/integrations/api/v1/
- **OpenAPI specification:** https://app.linkila.com/integrations/api/v1/openapi.json
- **API base URL:** `https://app.linkila.com/integrations/api/v1`

## Authentication

### API Key

Authenticate to Linkila Public API v1 with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.linkila.com/integrations/api/v1/openapi.json)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Analytics By Interval](actions/count-analytics-by-interval.md) | `POST /analytics/countByInterval` | [docs](https://app.linkila.com/integrations/api/v1/) |
| [Create Redirection Session](actions/create-redirection-session.md) | `POST /createRedirectionSession` | [docs](https://app.linkila.com/integrations/api/v1/) |
| [Edit Link](actions/edit-link.md) | `POST /editLink/:link_id` | [docs](https://app.linkila.com/integrations/api/v1/) |
| [Get Access Log](actions/get-access-log.md) | `POST /analytics/accessLog` | [docs](https://app.linkila.com/integrations/api/v1/) |
| [Get Redirection](actions/get-redirection.md) | `POST /redirection` | [docs](https://app.linkila.com/integrations/api/v1/) |
| [List Domains](actions/list-domains.md) | `GET /domains` | [docs](https://app.linkila.com/integrations/api/v1/) |
| [List Filters](actions/list-filters.md) | `GET /filters` | [docs](https://app.linkila.com/integrations/api/v1/) |
| [List Links](actions/list-links.md) | `GET /links` | [docs](https://app.linkila.com/integrations/api/v1/) |
| [Quick Generate Link](actions/quick-generate-link.md) | `POST /quickGenerate` | [docs](https://app.linkila.com/integrations/api/v1/) |
