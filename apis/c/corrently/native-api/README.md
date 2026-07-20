# Corrently: Native API Reference

A consolidated summary of Corrently's API configuration, with links to official documentation.

- **Official docs:** https://console.corrently.io/apis.html
- **API base URL:** `https://api.corrently.io/v2.0`

## Authentication

### API Key Token Exchange

Exchange the Corrently API key/appid for a short-lived Corrently access token before API requests.

### Credentials

- **API Key:** `apiKey` · required · Corrently API key/appid used to request a Corrently access token.

[Official authentication documentation](https://console.corrently.io/token.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.
