# Opportify: Native API Reference

A consolidated summary of Opportify's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://www.opportify.ai/docs
- **API base URL:** `https://api.opportify.ai/insights/v1`

## Authentication

### API Key

Use your Opportify Insights API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.opportify.ai/docs/api/api-reference/opportify-insights-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Email](actions/analyze-email.md) | `POST /email/analyze` | [docs](https://www.opportify.ai/docs/api/api-reference/analyze-email) |
| [Analyze IP](actions/analyze-ip.md) | `POST /ip/analyze` | [docs](https://www.opportify.ai/docs/api/api-reference/analyze-ip) |
| [Batch Analyze Emails](actions/batch-analyze-emails.md) | `POST /email/batch` | [docs](https://www.opportify.ai/docs/api/api-reference/batch-analyze-emails) |
| [Batch Analyze IPs](actions/batch-analyze-ips.md) | `POST /ip/batch` | [docs](https://www.opportify.ai/docs/api/api-reference/batch-analyze-ips) |
| [Create Email Batch Export](actions/create-email-batch-export.md) | `POST /email/batch/:jobId/exports` | [docs](https://www.opportify.ai/docs/api/api-reference/create-email-batch-export) |
| [Create IP Batch Export](actions/create-ip-batch-export.md) | `POST /ip/batch/:jobId/exports` | [docs](https://www.opportify.ai/docs/api/api-reference/create-ip-batch-export) |
| [Get Email Batch Export Status](actions/get-email-batch-export-status.md) | `GET /email/batch/:jobId/exports/:exportId` | [docs](https://www.opportify.ai/docs/api/api-reference/get-email-batch-export-status) |
| [Get Email Batch Status](actions/get-email-batch-status.md) | `GET /email/batch/:jobId` | [docs](https://www.opportify.ai/docs/api/api-reference/get-email-batch-status) |
| [Get IP Batch Export Status](actions/get-ip-batch-export-status.md) | `GET /ip/batch/:jobId/exports/:exportId` | [docs](https://www.opportify.ai/docs/api/api-reference/get-ip-batch-export-status) |
| [Get IP Batch Status](actions/get-ip-batch-status.md) | `GET /ip/batch/:jobId` | [docs](https://www.opportify.ai/docs/api/api-reference/get-ip-batch-status) |
