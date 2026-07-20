# Screenshotbase: Native API Reference

A consolidated summary of Screenshotbase's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://screenshotbase.com/docs/
- **API base URL:** `https://api.screenshotbase.com/v1`

## Authentication

### API Key

Connect with a Screenshotbase API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
apikey: <apiKey>
```

[Official authentication documentation](https://screenshotbase.com/docs/authentication)

### API Key Header

Connect with a Screenshotbase API key using the required apikey header.

Send these headers with each API request:

```http
apikey: <apiKey>
```

[Official authentication documentation](https://screenshotbase.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check API Status](actions/check-api-status.md) | `GET /status` | [docs](https://screenshotbase.com/docs/status) |
| [Take Website Screenshot](actions/take-website-screenshot.md) | `GET /take` | [docs](https://screenshotbase.com/docs/take) |
