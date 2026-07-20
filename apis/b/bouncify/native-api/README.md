# Bouncify: Native API Reference

A consolidated summary of Bouncify's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://bouncify.io/docs/api-docs/
- **API base URL:** `https://api.bouncify.io/v1`

## Authentication

### Bouncify API Key

Use your Bouncify API key. Bouncify requires the key on every request as the documented query parameter `apikey`.

### Credentials

- **API Key:** `apiKey` · required · Your Bouncify API key.

[Official authentication documentation](https://bouncify.io/docs/api-docs/api-usage/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Job Status](actions/check-job-status.md) | `GET /bulk/:job_id` | [docs](https://bouncify.io/docs/api-docs/bulk-validation/check-job-status/) |
| [Delete Bulk Email List](actions/delete-bulk-email-list.md) | `DELETE /bulk/:job_id` | [docs](https://bouncify.io/docs/api-docs/bulk-validation/delete-list/) |
| [Download Verification Result](actions/download-verification-result.md) | `POST /download` | [docs](https://bouncify.io/docs/api-docs/bulk-validation/download-result/) |
| [Get Credit Balance](actions/get-credit-balance.md) | `GET /info` | [docs](https://bouncify.io/docs/api-docs/account/) |
| [Start Verifying Bulk List](actions/start-verifying-bulk-list.md) | `PATCH /bulk/:job_id` | [docs](https://bouncify.io/docs/api-docs/bulk-validation/start-verifying-bulk-email-list/) |
| [Upload Bulk Email List](actions/upload-bulk-email-list.md) | `POST /bulk` | [docs](https://bouncify.io/docs/api-docs/bulk-validation/upload-bulk-email-list/) |
| [Validate Email](actions/validate-email.md) | `GET /verify` | [docs](https://bouncify.io/docs/api-docs/single-validation/) |
