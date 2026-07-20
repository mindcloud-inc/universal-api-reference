# MillionVerifier: Native API Reference

A consolidated summary of MillionVerifier's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://developer.millionverifier.com/
- **API base URL:** `https://api.millionverifier.com`

## Authentication

### API Key

Connect with a MillionVerifier API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.millionverifier.com/email-verification-api/manage-api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–50). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Verification File](actions/delete-verification-file.md) | `GET https://bulkapi.millionverifier.com/bulkapi/v2/delete` | [docs](https://developer.millionverifier.com/#operation/bulk-delete) |
| [Download Verification Report](actions/download-verification-report.md) | `GET https://bulkapi.millionverifier.com/bulkapi/v2/download` | [docs](https://developer.millionverifier.com/#operation/bulk-download) |
| [Get API Credits](actions/get-api-credits.md) | `GET /api/v3/credits` | [docs](https://developer.millionverifier.com/#operation/api-credits) |
| [Get Verification File](actions/get-verification-file.md) | `GET https://bulkapi.millionverifier.com/bulkapi/v2/fileinfo` | [docs](https://developer.millionverifier.com/#operation/bulk-fileinfo) |
| [List Verification Files](actions/list-verification-files.md) | `GET https://bulkapi.millionverifier.com/bulkapi/v2/filelist` | [docs](https://developer.millionverifier.com/#operation/bulk-filelist) |
| [Stop Verification File](actions/stop-verification-file.md) | `GET https://bulkapi.millionverifier.com/bulkapi/stop` | [docs](https://developer.millionverifier.com/#operation/bulk-stop) |
| [Upload Verification File](actions/upload-verification-file.md) | `POST https://bulkapi.millionverifier.com/bulkapi/v2/upload` | [docs](https://developer.millionverifier.com/#operation/bulk-upload) |
| [Verify Email](actions/verify-email.md) | `GET /api/v3` | [docs](https://developer.millionverifier.com/#operation/single-verification) |
