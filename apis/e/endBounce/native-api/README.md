# EndBounce: Native API Reference

A consolidated summary of EndBounce's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://app.endbounce.com/integrations
- **API base URL:** `https://api.endbounce.com/api/integrations`

## Authentication

### API Key

Authenticate EndBounce API requests with the account API key sent in the X-API-Key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://app.endbounce.com/integrations)

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Find Email](actions/find-email.md) | `POST /v1/finder` | [docs](https://app.endbounce.com/integrations) |
| [Get Verification Job Results](actions/get-verification-job-results.md) | `GET /v1/jobs/:request_id/results` | [docs](https://app.endbounce.com/integrations) |
| [Get Verification Job Status](actions/get-verification-job-status.md) | `GET /v1/jobs/:request_id/status` | [docs](https://app.endbounce.com/integrations) |
| [Verify Email](actions/verify-email.md) | `POST /v1/verify` | [docs](https://app.endbounce.com/integrations) |
| [Verify Emails Batch](actions/verify-emails-batch.md) | `POST /v1/verify` | [docs](https://app.endbounce.com/integrations) |
