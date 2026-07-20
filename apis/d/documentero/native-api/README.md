# Documentero: Native API Reference

A consolidated summary of Documentero's API configuration, with links to official documentation.

- **Official docs:** https://docs.documentero.com/documentation/api/
- **API base URL:** `https://app.documentero.com/api`

## Authentication

### API Key

Connect using your Documentero API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.documentero.com/documentation/api/integrate-with-documentero-cloud-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
