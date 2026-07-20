# Agicap: Native API Reference

A consolidated summary of Agicap's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://api.agicap.com/treasury-bank-journal/detailed_documentation.pdf
- **API base URL:** `https://api.agicap.com`

## Authentication

### OAuth2 Client Credentials

Authenticate with Agicap's OAuth2 client-credentials token endpoint.

### Credentials

- **Organization ID:** `organizationId` · required · Agicap organization UUID displayed on the Public API clients/settings page. Used by organization-scoped public API endpoints.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.agicap.com/public/auth/v1/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `agicap:public-api`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://api.agicap.com/treasury-bank-journal/detailed_documentation.pdf)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bank Journal Export](actions/create-bank-journal-export.md) | `POST /public/treasury-bank-journal/v1/entities/:entityId/exports/:exportId` | [docs](https://api.agicap.com/treasury-bank-journal/detailed_documentation.pdf) |
| [Get Bank Journal Export Details](actions/get-bank-journal-export-details.md) | `GET /public/treasury-bank-journal/v1/entities/:entityId/exports/:exportId` | [docs](https://api.agicap.com/treasury-bank-journal/detailed_documentation.pdf) |
| [List Bank Journal Exports](actions/list-bank-journal-exports.md) | `GET /public/treasury-bank-journal/v1/entities/:entityId/exports` | [docs](https://api.agicap.com/treasury-bank-journal/detailed_documentation.pdf) |
| [List Organization Entities](actions/list-organization-entities.md) | `GET /public/organizations/v1/:organizationId/entities` | [docs](https://api.agicap.com/treasury-bank-journal/detailed_documentation.pdf) |
