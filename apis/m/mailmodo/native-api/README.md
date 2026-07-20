# Mailmodo: Native API Reference

A consolidated summary of Mailmodo's API configuration, with links to official documentation.

- **Official docs:** https://support.mailmodo.com/articles/238356-api-reference-guide
- **API base URL:** `https://api.mailmodo.com`

## Authentication

### API Key

Connect Mailmodo with an API key from Mailmodo Settings -> API Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.mailmodo.com/articles/238356-api-reference-guide)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.
