# HeyGen: Native API Reference

A consolidated summary of HeyGen's API configuration, with links to official documentation.

- **Official docs:** https://docs.heygen.com/reference
- **API base URL:** `https://api.heygen.com`

## Authentication

### Direct API Key

Send only the HeyGen X-Api-Key header without implicit bearer auth.

### Credentials

- **API Key:** `apiKey` · optional · Stored HeyGen direct API key for header injection through request templates.

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://docs.heygen.com/docs/quick-start)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.
