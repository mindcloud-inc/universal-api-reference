# Focusmate: Native API Reference

A consolidated summary of Focusmate's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.focusmate.com/
- **API base URL:** `https://api.focusmate.com/v1`

## Authentication

### API Key

Use a Focusmate Public API key sent in the X-API-KEY request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://apidocs.focusmate.com/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `408,429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | `GET /me` | [docs](https://apidocs.focusmate.com/) |
| [Get Partner Profile](actions/get-partner-profile.md) | `GET /users/:userId` | [docs](https://apidocs.focusmate.com/) |
| [Get Sessions](actions/get-sessions.md) | `GET /sessions` | [docs](https://apidocs.focusmate.com/) |
