# Buzzsprout: Native API Reference

A consolidated summary of Buzzsprout's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://github.com/buzzsprout/buzzsprout-api
- **API base URL:** `https://www.buzzsprout.com/api`

## Authentication

### API Key

Connect with a Buzzsprout API token and podcast ID.

### Credentials

- **API Key:** `apiKey` · required
- **Podcast ID:** `podcastId` · required · Numeric Buzzsprout podcast identifier used in episode API paths.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://github.com/buzzsprout/buzzsprout-api#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |
| `User-Agent` | `MindCloud/1.0` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Podcasts](actions/list-podcasts.md) | `GET /podcasts.json` | [docs](https://raw.githubusercontent.com/buzzsprout/buzzsprout-api/master/sections/podcasts.md) |
