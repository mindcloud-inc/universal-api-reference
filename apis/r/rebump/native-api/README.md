# Rebump: Native API Reference

A consolidated summary of Rebump's API configuration, with links to official documentation.

- **Official docs:** https://www.rebump.cc/docs/api
- **API base URL:** `https://www.rebump.cc/`

## Authentication

### API Access

Rebump API access uses an API key plus an Access ID that corresponds to the Rebump account email address.

### Credentials

- **API Key:** `apiKey` · required
- **Access ID:** `accessId` · required · Rebump account email address sent in the x-access-id header.

Send these headers with each API request:

```http
x-access-id: <accessId>
x-access-token: <apiKey>
```

[Official authentication documentation](https://site.rebump.cc/integrating-rebump-with-your-crm/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.
