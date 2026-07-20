# Moblico: Native API Reference

A consolidated summary of Moblico's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://client.moblico.net/developer/trialtpl/signup.jsp
- **REST API base URL:** `https://moblico.net/services/v4`
- **AUTH base URL:** `https://client.moblico.net/services/v4`

## Authentication

### Moblico Token

Authenticates with a Moblico API key, username, and password to obtain a user token.

### Credentials

- **API Key:** `apiKey` · required · Moblico API key used by GET /authenticate.
- **Username:** `username` · required · Moblico username used by GET /authenticate.
- **Password:** `password` · required · Moblico password used by GET /authenticate.

[Official authentication documentation](https://client.moblico.net/developer/trialtpl/signup.jsp)

## API conventions

### REST API

Shared parameters:

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `token` | query | `string` | no |

## Retry behavior

- **REST API:** Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check User Exists](actions/check-user-exists.md) | `GET /users/exists` | [docs](https://client.moblico.net/developer/trialtpl/signup.jsp) |
| [Create User ID](actions/create-user-id.md) | `GET /users/createId` | [docs](https://client.moblico.net/developer/trialtpl/signup.jsp) |
| [Get User](actions/get-user.md) | `GET /users/:username` | [docs](https://client.moblico.net/developer/trialtpl/signup.jsp) |
