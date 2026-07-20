# Uplisting: Native API Reference

A consolidated summary of Uplisting's API configuration, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/1320372/SWTBfdW6
- **API base URL:** `https://connect.uplisting.io`

## Authentication

### API Key

Use your Uplisting API key with a Basic Authorization header.

### Credentials

- **API Key:** `apiKey` · required
- **Client ID:** `clientId` · optional · Optional Uplisting partner Client ID required for v2 endpoints such as custom booking attributes and booking creation.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.uplisting.io/docs/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
