# Once.to: Native API Reference

A consolidated summary of Once.to's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://docs.once.to/en/api/v1/
- **API base URL:** `https://once.to/api/public/v1`

## Authentication

### API Key

Authenticate Once.to requests with an API key in the X-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.once.to/en/kb/api-keys/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Short Link](actions/create-short-link.md) | `POST /links` | [docs](https://docs.once.to/en/api/v1/endpoints/links-post/) |
| [Get Current User](actions/get-current-user.md) | `GET /auth` | [docs](https://docs.once.to/en/api/v1/endpoints/auth-get/) |
| [Get Domain](actions/get-domain.md) | `GET /domains/:id` | [docs](https://docs.once.to/en/api/v1/endpoints/domains-get-by-id/) |
| [Get Link](actions/get-link.md) | `GET /links/:id` | [docs](https://docs.once.to/en/api/v1/endpoints/links-get-by-id/) |
| [List Domains](actions/list-domains.md) | `GET /domains` | [docs](https://docs.once.to/en/api/v1/endpoints/domains-get/) |
| [List Links](actions/list-links.md) | `GET /links` | [docs](https://docs.once.to/en/api/v1/endpoints/links-get/) |
| [Update Domain Settings](actions/update-domain-settings.md) | `PUT /domains/:id` | [docs](https://docs.once.to/en/api/v1/endpoints/domains-put/) |
