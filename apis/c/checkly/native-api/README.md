# Checkly: Native API Reference

A consolidated summary of Checkly's API configuration, with links to official documentation.

- **Official docs:** https://www.checklyhq.com/docs/api-reference/overview/
- **OpenAPI specification:** https://checklyhq.com/docs/api-reference/openapi.json
- **API base URL:** `https://api.checklyhq.com`

## Authentication

### API Key

Use a Checkly API key plus account ID. The runtime sends the API key as a bearer token and the account ID in the X-Checkly-Account header.

### Credentials

- **API Key:** `apiKey` · required · Your Checkly API key.
- **Account ID:** `accountId` · required · Your Checkly account ID.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
X-Checkly-Account: <accountId>
```

[Official authentication documentation](https://www.checklyhq.com/docs/api-reference/overview/)
