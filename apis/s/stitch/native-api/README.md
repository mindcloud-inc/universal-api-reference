# Stitch: Native API Reference

A consolidated summary of Stitch's API configuration, with links to official documentation.

- **Official docs:** https://www.stitchdata.com/docs/developers/stitch-connect/api#authentication-overview
- **API base URL:** `https://api.stitchdata.com`

## Authentication

### API Token

Authenticate Stitch Connect API requests with a bearer access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.stitchdata.com/docs/developers/stitch-connect/api#authentication-overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
