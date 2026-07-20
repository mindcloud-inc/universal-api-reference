# Klaviyo: Native API Reference

A consolidated summary of Klaviyo's API configuration, with links to official documentation.

- **Official docs:** https://developers.klaviyo.com/en/reference/api_overview
- **OpenAPI specification:** https://raw.githubusercontent.com/klaviyo/openapi/main/openapi/stable.json
- **API base URL:** `https://a.klaviyo.com/api/`

## Authentication

### API Key

Private API key authentication for server-side Klaviyo API access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Klaviyo-API-Key <apiKey>
```

[Official authentication documentation](https://developers.klaviyo.com/en/docs/authenticate_)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |
| `Content-Type` | `application/json; charset=utf-8` |
| `revision` | `2024-10-15` |

Responses from this API use JSON. Response data is read from `data`.
