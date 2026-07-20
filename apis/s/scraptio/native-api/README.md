# Scraptio: Native API Reference

A consolidated summary of Scraptio's API configuration, with links to official documentation.

- **Official docs:** https://scraptio.notion.site/Scraptio-Docs-6414064fb16342098de4e251cf9f89f5
- **API base URL:** `https://api.scraptio.com`

## Authentication

### Custom Header API Key

### Credentials

- **x-api-key:** `xApiKey` · optional · Stored Scraptio API key value used for header injection.

Send these headers with each API request:

```http
X-API-KEY: <xApiKey>
```

[Official authentication documentation](https://scraptio.notion.site/how-to-use-scraptio-with-rest-api-caf0b6d5c6e342cd9a3ac9062ab1ae6d)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
