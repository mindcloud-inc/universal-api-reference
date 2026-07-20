# Availity: Native API Reference

A consolidated summary of Availity's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://developer.availity.com/blog/2025/3/25/hipaa-transactions
- **API base URL:** `https://api.availity.com`

## Authentication

### OAuth2 Client Credentials

OAuth2 client credentials authentication for Availity REST APIs.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.availity.com/v1/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `healthcare-hipaa-transactions-demo`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://developer.availity.com/blog/2025/10/31/availity-api-guide)

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–50). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Claim Status Inquiry](actions/create-claim-status-inquiry.md) | `POST /availity/v1/claim-statuses` | [docs](https://developer.availity.com/blog/2025/3/25/hipaa-transactions) |
| [Create Coverage Inquiry](actions/create-coverage-inquiry.md) | `POST /v1/coverages` | [docs](https://developer.availity.com/blog/2025/3/25/hipaa-transactions) |
| [Create Institutional Predetermination](actions/create-institutional-predetermination.md) | `POST /availity/v1/institutional-claims` | [docs](https://developer.availity.com/blog/2025/3/25/hipaa-transactions) |
| [Create Professional Cost Estimate](actions/create-professional-cost-estimate.md) | `POST /availity/v2/patient-cost-estimates/prof` | [docs](https://developer.availity.com/blog/2025/3/25/hipaa-transactions) |
| [Create Professional Predetermination](actions/create-professional-predetermination.md) | `POST /availity/v1/professional-claims` | [docs](https://developer.availity.com/blog/2025/3/25/hipaa-transactions) |
| [Delete Claim Status Inquiry](actions/delete-claim-status-inquiry.md) | `DELETE /availity/v1/claim-statuses/{id}` | [docs](https://developer.availity.com/blog/2025/3/25/hipaa-transactions) |
| [Delete Coverage Inquiry](actions/delete-coverage-inquiry.md) | `DELETE /v1/coverages/{id}` | [docs](https://developer.availity.com/blog/2025/3/25/hipaa-transactions) |
| [Get Claim Status Inquiry](actions/get-claim-status-inquiry.md) | `GET /availity/v1/claim-statuses/{id}` | [docs](https://developer.availity.com/blog/2025/3/25/hipaa-transactions) |
| [Get Coverage Inquiry](actions/get-coverage-inquiry.md) | `GET /v1/coverages/{id}` | [docs](https://developer.availity.com/blog/2025/3/25/hipaa-transactions) |
| [Get Institutional Predetermination](actions/get-institutional-predetermination.md) | `GET /availity/v1/institutional-claims/{id}` | [docs](https://developer.availity.com/blog/2025/3/25/hipaa-transactions) |
| [Get Professional Cost Estimate](actions/get-professional-cost-estimate.md) | `GET /availity/v2/patient-cost-estimates/prof/{id}` | [docs](https://developer.availity.com/blog/2025/3/25/hipaa-transactions) |
| [Get Professional Predetermination](actions/get-professional-predetermination.md) | `GET /availity/v1/professional-claims/{id}` | [docs](https://developer.availity.com/blog/2025/3/25/hipaa-transactions) |
| [List Payers](actions/list-payers.md) | `GET /v1/availity-payer-list` | [docs](https://developer.availity.com/blog/2025/3/25/hipaa-transactions) |
