# ProcurementExpress.com: Native API Reference

A consolidated summary of ProcurementExpress.com's API configuration, with links to official documentation.

- **Official docs:** https://docs.procurementexpress.com
- **API base URL:** `https://app.procurementexpress.com`

## Authentication

### OAuth 2.0

Connect ProcurementExpress.com using OAuth application credentials and bearer tokens.

### Credentials

- **App Company ID:** `appCompanyId` · required · The ProcurementExpress.com company ID to send with API requests.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://app.procurementexpress.com/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `public`.

Refresh expired access tokens with a POST request to https://app.procurementexpress.com/oauth/token. A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.procurementexpress.com)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `per_page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.
