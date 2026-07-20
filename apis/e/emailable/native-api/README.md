# Emailable: Native API Reference

A consolidated summary of Emailable's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://emailable.com/docs/api/
- **API base URL:** `https://api.emailable.com`

## Authentication

### API Key

Use a private Emailable API key to authenticate requests to the Emailable REST API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://emailable.com/docs/api/#authentication)

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Verification Batch](actions/create-verification-batch.md) | `POST /v1/batch` | [docs](https://emailable.com/docs/api/#verify-a-batch-of-emails) |
| [Get Account Info](actions/get-account-info.md) | `GET /v1/account` | [docs](https://emailable.com/docs/api/#get-account-info) |
| [Get Batch Status](actions/get-batch-status.md) | `GET /v1/batch` | [docs](https://emailable.com/docs/api/#get-the-status-of-a-batch) |
| [Verify Email](actions/verify-email.md) | `GET /v1/verify` | [docs](https://emailable.com/docs/api/#verify-an-email) |
