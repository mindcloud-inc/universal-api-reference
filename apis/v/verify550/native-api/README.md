# Verify550: Native API Reference

A consolidated summary of Verify550's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://verify550.com/documentation/api/
- **API base URL:** `https://app.verify550.com/api`

## Authentication

### API Key

Use your Verify550 API key passed as the secret query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://verify550.com/documentation/api/)

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Download Processed File](actions/download-processed-file.md) | `GET /file` | [docs](https://verify550.com/documentation/endpoint-specifications/) |
| [Download Ready File](actions/download-ready-file.md) | `GET /details` | [docs](https://verify550.com/documentation/api/) |
| [Download Verification Results](actions/download-verification-results.md) | `GET /jobexport/:jobId` | [docs](https://verify550.com/documentation/api/) |
| [Get Verification Job](actions/get-verification-job.md) | `GET /getjob/:jobId` | [docs](https://verify550.com/documentation/api/) |
| [Upload Bulk Email File](actions/upload-bulk-email-file.md) | `POST /bulk` | [docs](https://verify550.com/documentation/api/) |
| [Upload Bulk Phone File](actions/upload-bulk-phone-file.md) | `POST /bulkPhoneList` | [docs](https://verify550.com/documentation/validating-phone-numbers-using-the-verify550-api-2/) |
| [Verify Single Email](actions/verify-single-email.md) | `GET /singlemail` | [docs](https://verify550.com/documentation/api/) |
