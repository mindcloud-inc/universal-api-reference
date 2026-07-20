# innoChat: Native API Reference

A consolidated summary of innoChat's API configuration, with links to official documentation.

- **Official docs:** https://docs.innochat.ch/api-reference
- **API base URL:** `https://app.innochat.ch/api/v1`

## Authentication

### API Key

Authenticate with an INNOCHAT API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.innochat.ch/api-reference/api-key-setup)
