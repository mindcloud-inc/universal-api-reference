# Alt Text Generator: Native API Reference

A consolidated summary of Alt Text Generator's API configuration, with links to official documentation.

- **Official docs:** https://www.alttextlab.com/docs
- **API base URL:** `https://app.alttextlab.com`

## Authentication

### AltTextLab Header API Key

Authenticate AltTextLab by sending your API key only in the x-api-key header.

### Credentials

- **API Key:** `apiKey` · optional · Your AltTextLab API key used to populate the x-api-key header.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://www.alttextlab.com/docs/api-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.
