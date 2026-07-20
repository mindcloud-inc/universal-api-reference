# Vector Vault: Native API Reference

A consolidated summary of Vector Vault's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://github.com/John-Rood/VectorVault/tree/main/docs
- **API base URL:** `https://api.vectorvault.io`

## Authentication

### Email + API Key

Sign in with your Vector Vault account email and API key.

### Credentials

- **Email:** `email` · required · The email address tied to your Vector Vault API key.
- **API Key:** `apiKey` · required · Your Vector Vault tenant API key.

Send these headers with each API request:

```http
Authorization: Bearer <custom.access_token>
```

[Official authentication documentation](https://github.com/John-Rood/VectorVault/blob/main/README.md#core-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | `POST login_with_api` | [docs](https://github.com/John-Rood/VectorVault/blob/main/README.md#core-api) |
| [List Vaults](actions/list-vaults.md) | `POST get_vaults` | [docs](https://github.com/John-Rood/VectorVault/blob/main/README.md#core-api) |
