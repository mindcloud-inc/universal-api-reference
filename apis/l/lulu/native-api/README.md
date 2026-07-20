# Lulu: Native API Reference

A consolidated summary of Lulu's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://api.lulu.com/docs/
- **OpenAPI specification:** https://api.lulu.com/api-docs/openapi-specs/openapi_public.yml
- **API base URL:** `{apiBaseUrl}`

## Authentication

### OAuth2 Client Credentials

Use Lulu OAuth2 client credentials. Store environment-specific API and token URLs in the credential so the same app supports sandbox and production.

### Credentials

- **Client ID:** `clientId` · required · Your Lulu OAuth2 client ID.
- **API Base URL:** `apiBaseUrl` · required · Use https://api.lulu.com for production or https://api.sandbox.lulu.com for sandbox.
- **Token URL:** `tokenUrl` · required · Use the matching Lulu Keycloak token URL for your environment.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to {{credentials.tokenUrl}}.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://api.lulu.com/docs/)

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Calculate Cover Dimensions](actions/calculate-cover-dimensions.md) | `POST /cover-dimensions/` | [docs](https://api.lulu.com/docs/#tag/Cover-Dimensions/operation/Cover-Dimensions_create) |
| [Cancel Print Job](actions/cancel-print-job.md) | `PUT /print-jobs/{id}/status/` | [docs](https://api.lulu.com/docs/#tag/Print-Jobs/operation/Print-Jobs_status_cancel) |
| [Create Print Job](actions/create-print-job.md) | `POST /print-jobs/` | [docs](https://api.lulu.com/docs/#tag/Print-Jobs/operation/Print-Jobs_create) |
| [Create Print Job Cost Calculation](actions/create-print-job-cost-calculation.md) | `POST /print-job-cost-calculations/` | [docs](https://api.lulu.com/docs/#tag/Print-Job-Cost-Calculations/operation/Print-Job-cost-calculations_create) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks/` | [docs](https://api.lulu.com/docs/#tag/Webhooks/operation/subscribe-webhooks) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/{id}/` | [docs](https://api.lulu.com/docs/#tag/Webhooks/operation/delete-webhook) |
| [Get Cover Validation](actions/get-cover-validation.md) | `GET /validate-cover/{id}/` | [docs](https://api.lulu.com/docs/#tag/Validate-Cover/operation/Validate-Cover_read) |
| [Get Interior Validation](actions/get-interior-validation.md) | `GET /validate-interior/{id}/` | [docs](https://api.lulu.com/docs/#tag/Validate-Interior/operation/Validate-Interior_read) |
| [Get Print Job](actions/get-print-job.md) | `GET /print-jobs/{id}/` | [docs](https://api.lulu.com/docs/#tag/Print-Jobs/operation/Print-Jobs_read) |
| [Get Print Job Costs](actions/get-print-job-costs.md) | `GET /print-jobs/{id}/costs/` | [docs](https://api.lulu.com/docs/#tag/Print-Jobs/operation/Print-Jobs_costs) |
| [Get Print Job Statistics](actions/get-print-job-statistics.md) | `GET /print-jobs/statistics/` | [docs](https://api.lulu.com/docs/#tag/Print-Jobs/operation/Print-Jobs_statistics) |
| [Get Print Job Status](actions/get-print-job-status.md) | `GET /print-jobs/{id}/status/` | [docs](https://api.lulu.com/docs/#tag/Print-Jobs/operation/Print-Jobs_status_read) |
| [Get Shipping Options](actions/get-shipping-options.md) | `POST /shipping-options/` | [docs](https://api.lulu.com/docs/#tag/Shipping-Options/operation/retrieve-shipping-options) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/{id}/` | [docs](https://api.lulu.com/docs/#tag/Webhooks/operation/retrieve-webhook) |
| [List Print Jobs](actions/list-print-jobs.md) | `GET /print-jobs/` | [docs](https://api.lulu.com/docs/#tag/Print-Jobs/operation/Print-Jobs_list) |
| [List Webhook Submissions](actions/list-webhook-submissions.md) | `GET /webhook-submissions/` | [docs](https://api.lulu.com/docs/#tag/Webhooks/operation/retrieve-webhook-submissions) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks/` | [docs](https://api.lulu.com/docs/#tag/Webhooks/operation/retrieve-webhooks) |
| [Reprint Print Job](actions/reprint-print-job.md) | `POST /print-jobs/` | [docs](https://api.lulu.com/docs/#tag/Print-Jobs/operation/Print-Jobs_reprint) |
| [Test Webhook Submission](actions/test-webhook-submission.md) | `POST /webhooks/{id}/test-submission/{topic}/` | [docs](https://api.lulu.com/docs/#tag/Webhooks/operation/test-webhook-submission) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /webhooks/{id}/` | [docs](https://api.lulu.com/docs/#tag/Webhooks/operation/update-webhook) |
| [Validate Cover](actions/validate-cover.md) | `POST /validate-cover/` | [docs](https://api.lulu.com/docs/#tag/Validate-Cover/operation/Validate-Cover_create) |
| [Validate Interior](actions/validate-interior.md) | `POST /validate-interior/` | [docs](https://api.lulu.com/docs/#tag/Validate-Interior/operation/Validate-Interior_create) |
