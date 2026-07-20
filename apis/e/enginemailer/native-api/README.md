# Enginemailer: Native API Reference

A consolidated summary of Enginemailer's API configuration, with links to official documentation.

- **Official docs:** https://enginemailer.zendesk.com/hc/en-us
- **API base URL:** `https://api.enginemailer.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
APIKey: <apiKey>
```

[Official authentication documentation](https://enginemailer.zendesk.com/hc/en-us/articles/360000733792-Subscriber-REST-API-GETTING-STARTED)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
