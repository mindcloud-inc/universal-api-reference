# URL.dev: Native API Reference

A consolidated summary of URL.dev's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.superuser.app/readme.md
- **API base URL:** `https://v-20260317--open-meteo--superuser.su.dev`

## Authentication

### API Keychain secret

Authenticate Superuser toolkit requests with an API keychain secret as a Bearer token.

### Credentials

- **API keychain secret:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.superuser.app/hosted-tools/publishing-tools-via-command-line/api-keychain-specification.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current Weather](actions/get-current-weather.md) | `GET /current/` | [docs](https://superuser.app/org/superuser/toolkits/open-meteo/v-20260317/functions/current.js?method=GET) |
