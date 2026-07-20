# FLOWii: Native API Reference

A consolidated summary of FLOWii's API configuration, with links to official documentation.

- **Official docs:** https://flowiiapi.docs.apiary.io/reference
- **API base URL:** `https://api.flowii.com`

## Authentication

### FLOWii Token

Use a FLOWii API key together with a bearer access token. FLOWii business endpoints require both values on each request.

### Credentials

- **API Key:** `apiKey` · required · The FLOWii tenant API key.
- **Access Token:** `accessToken` · required · A valid FLOWii bearer token from POST /token.

Send these headers with each API request:

```http
Api-Key: <apiKey>
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://www.flowii.com/sk/manual/api/)
