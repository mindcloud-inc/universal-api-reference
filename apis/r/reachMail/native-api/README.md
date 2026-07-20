# ReachMail: Native API Reference

A consolidated summary of ReachMail's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://services.reachmail.net/
- **API base URL:** `https://services.reachmail.net`

## Authentication

### API Token

Authenticate ReachMail with a bearer API authorization token generated from the ReachMail account UI.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://services.reachmail.net/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | `GET /Administration/Users/Current` | [docs](https://services.reachmail.net/#resources/Administration/Users/Current) |
