# ApiFlash: Native API Reference

A consolidated summary of ApiFlash's API configuration, with links to official documentation.

- **Official docs:** https://apiflash.com/documentation
- **API base URL:** `https://api.apiflash.com`

## Authentication

### API Key

Authenticate with an ApiFlash access key from the ApiFlash dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apiflash.com/documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.
