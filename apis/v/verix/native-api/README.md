# Verix: Native API Reference

A consolidated summary of Verix's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://docs.verix.io/verifiable_credentials_apis/
- **OpenAPI specification:** https://docs.verix.io/verifiable_credentials_apis/api_doc.yml
- **API base URL:** `https://api.verix.io`

## Authentication

### Verix OAuth2 Client Credentials

### Credentials

- **Basic Authorization Header:** `basicAuth` · required · Paste the exact Verix Basic authorization header value from the Verix Integrations page.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://docs.verix.io/verifiable_credentials_apis/ to approve access.
2. Exchange the returned authorization code with a POST request to https://api.verix.io/v1/auth/token/.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.verix.io/verifiable_credentials_apis/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 10). Use `page_number` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Multiple Credentials](actions/create-multiple-credentials.md) | `POST /v1/credentials/groups/:group_id/` | [docs](https://docs.verix.io/verifiable_credentials_apis/) |
| [Delete Credential](actions/delete-credential.md) | `DELETE /v1/credentials/:credential_id/` | [docs](https://docs.verix.io/verifiable_credentials_apis/) |
| [Get Credential](actions/get-credential.md) | `GET /v1/credentials/:credential_id/` | [docs](https://docs.verix.io/verifiable_credentials_apis/) |
| [Get Group](actions/get-group.md) | `GET /v1/credentials/groups/:group_id/` | [docs](https://docs.verix.io/verifiable_credentials_apis/) |
| [List Credentials](actions/list-credentials.md) | `GET /v1/credentials` | [docs](https://docs.verix.io/verifiable_credentials_apis/) |
| [List Groups](actions/list-groups.md) | `GET /v1/credentials/groups` | [docs](https://docs.verix.io/verifiable_credentials_apis/) |
| [Update Multiple Credentials](actions/update-multiple-credentials.md) | `PUT /v1/credentials/groups/:group_id/` | [docs](https://docs.verix.io/verifiable_credentials_apis/) |
