# MailFloss: Native API Reference

A consolidated summary of MailFloss's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://developers.mailfloss.com
- **OpenAPI specification:** https://api.mailfloss.com/swagger_latest.json
- **API base URL:** `https://api.mailfloss.com`

## Authentication

### API Key

Connect MailFloss with an API key from the MailFloss dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.mailfloss.com/authentication)

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Batch Verification Job](actions/cancel-batch-verification-job.md) | `POST /batch-verify/:id/cancel` | [docs](https://developers.mailfloss.com/9bbG-reference) |
| [Change Integration Setting](actions/change-integration-setting.md) | `POST /settings/:id` | [docs](https://developers.mailfloss.com/reference) |
| [Create Batch Verification Job](actions/create-batch-verification-job.md) | `POST /batch-verify` | [docs](https://developers.mailfloss.com/9bbG-reference) |
| [Delete Emails](actions/delete-emails.md) | `POST /delete` | [docs](https://developers.mailfloss.com/privacy-reference) |
| [Get Batch Verification Results](actions/get-batch-verification-results.md) | `GET /batch-verify/:id/results` | [docs](https://developers.mailfloss.com/9bbG-reference) |
| [Get Batch Verification Status](actions/get-batch-verification-status.md) | `GET /batch-verify/:id/status` | [docs](https://developers.mailfloss.com/9bbG-reference) |
| [Verify Email Address](actions/verify-email-address.md) | `GET /verify` | [docs](https://developers.mailfloss.com/9bbG-reference) |
