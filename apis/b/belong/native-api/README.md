# Belong: Native API Reference

A consolidated summary of Belong's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://api.belong.net/api/v3/docs
- **OpenAPI specification:** https://api.belong.net/api/v3/openapi.json
- **API base URL:** `https://api.belong.net/api/v3`

## Authentication

### API Key

Connect using a Belong API key from your account settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://belongnet.github.io/docs/getting-started/api-docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The next-page cursor is read from `meta.pagination.endCursor`.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current User Profile](actions/get-current-user-profile.md) | `GET /me` | [docs](https://api.belong.net/api/v3/docs) |
| [Get Event](actions/get-event.md) | `GET /events/:id` | [docs](https://api.belong.net/api/v3/docs) |
| [Get Hub](actions/get-hub.md) | `GET /hubs/:id` | [docs](https://api.belong.net/api/v3/docs) |
| [Get Note](actions/get-note.md) | `GET /notes/:id` | [docs](https://api.belong.net/api/v3/docs) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://api.belong.net/api/v3/docs) |
| [List Hubs](actions/list-hubs.md) | `GET /hubs` | [docs](https://api.belong.net/api/v3/docs) |
| [List Notes](actions/list-notes.md) | `GET /notes` | [docs](https://api.belong.net/api/v3/docs) |
| [List Related Hubs](actions/list-related-hubs.md) | `GET /hubs/:id/related` | [docs](https://api.belong.net/api/v3/docs) |
| [Search Address Suggestions](actions/search-address-suggestions.md) | `GET /addresses/autocomplete` | [docs](https://api.belong.net/api/v3/docs) |
| [Search Nearby Events](actions/search-nearby-events.md) | `GET /events/nearby` | [docs](https://api.belong.net/api/v3/docs) |
