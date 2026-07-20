# Scalr: Native API Reference

A consolidated summary of Scalr's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.scalr.io/reference
- **OpenAPI specification:** https://scalr.io/api/iacp/v3/openapi-public.yml
- **API base URL:** `https://mindcloud.scalr.io/api/iacp/v3`

## Authentication

### API Token

Connect to Scalr with a personal or service-account API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.scalr.io/reference/api-tokens)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/vnd.api+json` |

## Pagination

Use `page[size]` in the query string to set the page size (default 20). Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Access Token](actions/create-access-token.md) | `POST /access-tokens` | [docs](https://docs.scalr.io/reference/create_access_token) |
| [Create Environment](actions/create-environment.md) | `POST /environments` | [docs](https://docs.scalr.io/reference/create_environment) |
| [Create Service Account](actions/create-service-account.md) | `POST /service-accounts` | [docs](https://docs.scalr.io/reference/create_service_account) |
| [Delete Access Token](actions/delete-access-token.md) | `DELETE /access-tokens/:access_token` | [docs](https://docs.scalr.io/reference/delete_access_token) |
| [Delete Environment](actions/delete-environment.md) | `DELETE /environments/:environment` | [docs](https://docs.scalr.io/reference/delete_environment) |
| [Delete Service Account](actions/delete-service-account.md) | `DELETE /service-accounts/:service_account` | [docs](https://docs.scalr.io/reference/delete_service_account) |
| [Get Access Token](actions/get-access-token.md) | `GET /access-tokens/:access_token` | [docs](https://docs.scalr.io/reference/get_access_token) |
| [Get Account](actions/get-account.md) | `GET /accounts/:account` | [docs](https://docs.scalr.io/reference/get_account) |
| [Get Account Metrics](actions/get-account-metrics.md) | `GET /accounts/:account/metrics` | [docs](https://docs.scalr.io/reference/get_metrics) |
| [Get Environment](actions/get-environment.md) | `GET /environments/:environment` | [docs](https://docs.scalr.io/reference/get_environment) |
| [Get Service Account](actions/get-service-account.md) | `GET /service-accounts/:service_account` | [docs](https://docs.scalr.io/reference/get_service_account) |
| [List Access Tokens](actions/list-access-tokens.md) | `GET /access-tokens` | [docs](https://docs.scalr.io/reference/list_access_tokens) |
| [List Account Users](actions/list-account-users.md) | `GET /account-users` | [docs](https://docs.scalr.io/reference/get_account_users) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://docs.scalr.io/reference/get_accounts) |
| [List Environments](actions/list-environments.md) | `GET /environments` | [docs](https://docs.scalr.io/reference/list_environments) |
| [List Service Accounts](actions/list-service-accounts.md) | `GET /service-accounts` | [docs](https://docs.scalr.io/reference/get_service_accounts) |
| [Lock Environment](actions/lock-environment.md) | `POST /environments/:environment/actions/lock` | [docs](https://docs.scalr.io/reference/lock_environment) |
| [Unlock Environment](actions/unlock-environment.md) | `POST /environments/:environment/actions/unlock` | [docs](https://docs.scalr.io/reference/unlock_environment) |
| [Update Access Token](actions/update-access-token.md) | `PATCH /access-tokens/:access_token` | [docs](https://docs.scalr.io/reference/update_access_token) |
| [Update Environment](actions/update-environment.md) | `PATCH /environments/:environment` | [docs](https://docs.scalr.io/reference/update_environment) |
