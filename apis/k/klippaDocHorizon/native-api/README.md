# Klippa DocHorizon: Native API Reference

A consolidated summary of Klippa DocHorizon's API configuration, with links to official documentation.

- **Official docs:** https://dochorizon.klippa.com/docs/api/getting-started
- **OpenAPI specification:** https://dochorizon.klippa.com/api/open-api.yaml
- **API base URL:** `https://dochorizon.klippa.com/api`

## Authentication

### API Key

Use a Klippa DocHorizon API key sent in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://dochorizon.klippa.com/docs/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
