# Kickbox: Native API Reference

A consolidated summary of Kickbox's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://docs.kickbox.com/docs/api-overview-copy
- **API base URL:** `https://api.kickbox.com/v2`

## Authentication

### API Key

Use a Kickbox API key for bearer authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.kickbox.com/docs/using-the-api)

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Batch Verification Status](actions/get-batch-verification-status.md) | `GET /verify-batch/:jobId` | [docs](https://docs.kickbox.com/docs/batch-verification-api) |
| [Start Batch Verification](actions/start-batch-verification.md) | `PUT /verify-batch` | [docs](https://docs.kickbox.com/docs/batch-verification-api) |
| [Verify Email](actions/verify-email.md) | `GET /verify` | [docs](https://docs.kickbox.com/docs/single-verification-api) |
