# RealFaviconGenerator: Native API Reference

A consolidated summary of RealFaviconGenerator's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://realfavicongenerator.net/developers
- **API base URL:** `https://realfavicongenerator.net/api`

## Authentication

### API Key

RealFaviconGenerator API key used in the favicon_generation json_params payload for interactive favicon generation.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://realfavicongenerator.net/developers/favicon-generation/interactive-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List change log](actions/list-change-log.md) | `GET /change-log` | [docs](https://realfavicongenerator.net/developers/change-log) |
| [List versions](actions/list-versions.md) | `GET /versions` | [docs](https://realfavicongenerator.net/developers/change-log) |
| [Start favicon generation](actions/start-favicon-generation.md) | `GET /favicon_generator` | [docs](https://realfavicongenerator.net/developers/favicon-generation/interactive-api) |
