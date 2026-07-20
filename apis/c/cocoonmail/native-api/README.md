# Cocoonmail: Native API Reference

A consolidated summary of Cocoonmail's API configuration, with links to official documentation.

- **Official docs:** https://kb.cocoonmail.com/api-view/api-introduction
- **API base URL:** `https://webhook.cocoonmail.com`

## Authentication

### API Key

Use a Cocoonmail API key. Cocoonmail requires the key to be sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://kb.cocoonmail.com/api-view/api-introduction)
