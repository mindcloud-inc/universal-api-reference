# OpenQR: Native API Reference

A consolidated summary of OpenQR's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://docs.openqr.io/
- **API base URL:** `https://api.openqr.io/api/v1`

## Authentication

### API Key

Authenticate OpenQR API requests with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.openqr.io/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `links.next`. The current page number is read from `meta.current_page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1. Follow the complete next-page URL returned by the API.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Call QR Code](actions/create-call-qr-code.md) | `POST /qr-codes` | [docs](https://docs.openqr.io/#tag/QR-Codes/operation/CreateQRCode) |
| [Create Folder](actions/create-folder.md) | `POST /folders` | [docs](https://docs.openqr.io/#tag/Folders/operation/CreateFolder) |
| [Create Static Text QR Code](actions/create-static-text-qr-code.md) | `POST /qr-codes` | [docs](https://docs.openqr.io/#tag/QR-Codes/operation/CreateQRCode) |
| [Create Static URL QR Code](actions/create-static-url-qr-code.md) | `POST /qr-codes` | [docs](https://docs.openqr.io/#tag/QR-Codes/operation/CreateQRCode) |
| [Create Text QR Code](actions/create-text-qr-code.md) | `POST /qr-codes` | [docs](https://docs.openqr.io/#tag/QR-Codes/operation/CreateQRCode) |
| [Create URL QR Code](actions/create-url-qr-code.md) | `POST /qr-codes` | [docs](https://docs.openqr.io/#tag/QR-Codes/operation/CreateQRCode) |
| [Get QR Code](actions/get-qr-code.md) | `GET /qr-codes/:qr_code_id` | [docs](https://docs.openqr.io/#tag/QR-Codes/operation/ViewQRCode) |
| [List Files](actions/list-files.md) | `GET /files/qr-logos` | [docs](https://docs.openqr.io/) |
| [List Folders](actions/list-folders.md) | `GET /folders` | [docs](https://docs.openqr.io/#tag/Folders/operation/GetFolders) |
| [List QR Codes](actions/list-qr-codes.md) | `GET /qr-codes` | [docs](https://docs.openqr.io/#tag/QR-Codes/operation/GetQRCodes) |
| [Update Folder](actions/update-folder.md) | `POST /folders/:folder_id` | [docs](https://docs.openqr.io/#tag/Folders/operation/UpdateFolder) |
| [Update QR Code](actions/update-qr-code.md) | `POST /qr-codes/:qr_code_id` | [docs](https://docs.openqr.io/#tag/QR-Codes/operation/UpdateQRCode) |
| [Upload File](actions/upload-file.md) | `POST /files/qr-logos` | [docs](https://docs.openqr.io/#tag/Files/operation/UploadFile) |
