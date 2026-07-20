# ConvertHub: Native API Reference

A consolidated summary of ConvertHub's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://converthub.com/api/docs
- **API base URL:** `https://api.converthub.com/v2`

## Authentication

### API Key

Authenticate requests with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://converthub.com/api/docs#authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Job](actions/cancel-job.md) | `DELETE /v2/jobs/:jobId` | [docs](https://converthub.com/api/docs) |
| [Check Conversion Support](actions/check-conversion-support.md) | `GET /v2/formats/:sourceFormat/to/:targetFormat` | [docs](https://converthub.com/api/docs) |
| [Complete Chunked Upload](actions/complete-chunked-upload.md) | `POST /v2/upload/:sessionId/complete` | [docs](https://converthub.com/api/docs) |
| [Convert File from Base64](actions/convert-file-from-base64.md) | `POST /v2/convert/base64` | [docs](https://converthub.com/api/docs) |
| [Convert File from URL](actions/convert-file-from-url.md) | `POST /v2/convert-url` | [docs](https://converthub.com/api/docs) |
| [Delete Conversion File](actions/delete-conversion-file.md) | `DELETE /v2/jobs/:jobId/destroy` | [docs](https://converthub.com/api/docs) |
| [Get Account Details](actions/get-account-details.md) | `GET /v2/account` | [docs](https://converthub.com/api/docs) |
| [Get All Supported Conversions](actions/get-all-supported-conversions.md) | `GET /v2/formats/supported-conversions` | [docs](https://converthub.com/api/docs) |
| [Get Download URL](actions/get-download-url.md) | `GET /v2/jobs/:jobId/download` | [docs](https://converthub.com/api/docs) |
| [Get Format Conversions](actions/get-format-conversions.md) | `GET /v2/formats/:format/conversions` | [docs](https://converthub.com/api/docs) |
| [Get Job Status](actions/get-job-status.md) | `GET /v2/jobs/:jobId` | [docs](https://converthub.com/api/docs) |
| [Get Supported Formats](actions/get-supported-formats.md) | `GET /v2/formats` | [docs](https://converthub.com/api/docs) |
| [Health Check](actions/health-check.md) | `GET /v2/health` | [docs](https://converthub.com/api/docs) |
| [Initialize Chunked Upload](actions/initialize-chunked-upload.md) | `POST /v2/upload/init` | [docs](https://converthub.com/api/docs) |
| [Submit File for Conversion](actions/submit-file-for-conversion.md) | `POST /v2/convert` | [docs](https://converthub.com/api/docs) |
| [Upload Chunk](actions/upload-chunk.md) | `POST /v2/upload/:sessionId/chunks/:chunkIndex` | [docs](https://converthub.com/api/docs) |
