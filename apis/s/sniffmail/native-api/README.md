# Sniffmail: Native API Reference

A consolidated summary of Sniffmail's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://sniffmail.io/docs
- **API base URL:** `https://api.sniffmail.io`

## Authentication

### API Key

Authenticate Sniffmail requests with your server-side API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://sniffmail.io/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Bulk Job](actions/create-bulk-job.md) | `POST /jobs` | [docs](https://sniffmail.io/docs) |
| [Get Job Results](actions/get-job-results.md) | `GET /jobs/:jobId/results` | [docs](https://sniffmail.io/docs) |
| [Get Job Status](actions/get-job-status.md) | `GET /jobs/:jobId` | [docs](https://sniffmail.io/docs) |
| [Validate Credentials](actions/validate-credentials.md) | `POST /verify` | [docs](https://sniffmail.io/docs) |
| [Verify Email](actions/verify-email.md) | `POST /verify` | [docs](https://sniffmail.io/docs) |
