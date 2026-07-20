# Businesslogic.online: Native API Reference

A consolidated summary of Businesslogic.online's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://api.businesslogic.online/describe
- **API base URL:** `https://api.businesslogic.online`

## Authentication

### Auth Token

Stores the Businesslogic X-Auth-Token value used on every API request.

### Credentials

- **Auth Token:** `authToken` · required · Businesslogic token sent as the exact `X-Auth-Token` header on every request.

Send these headers with each API request:

```http
X-Auth-Token: <authToken>
```

[Official authentication documentation](https://api.businesslogic.online/describe)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Describe Calculator](actions/describe-calculator.md) | `GET /describe` | [docs](https://api.businesslogic.online/describe) |
| [Execute Calculator](actions/execute-calculator.md) | `POST /execute` | [docs](https://api.businesslogic.online/execute) |
