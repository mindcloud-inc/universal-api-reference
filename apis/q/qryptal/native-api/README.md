# Qryptal: Native API Reference

A consolidated summary of Qryptal's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://dash2.qryptal.com/docs/api2-api/
- **API base URL:** `https://api2test.qryptal.com/v2/Vqodes/v2/Vqodes/`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dash2.qryptal.com/docs/api2-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Download QR Code Image](actions/download-qr-code-image.md) | `GET :uid/qr:uid.png` | [docs](https://dash2.qryptal.com/docs/api2-api/#created-qr-code) |
| [Generate EDC QR Code With Attachments](actions/generate-edc-qr-code-with-attachments.md) | `POST /` | [docs](https://dash2.qryptal.com/docs/api2-api/#api-call-generate-qr-edc) |
| [Generate PDC QR Code](actions/generate-pdc-qr-code.md) | `POST /` | [docs](https://dash2.qryptal.com/docs/api2-api/#api-call-generate-qr-pdc) |
| [Get QR Code Status](actions/get-qr-code-status.md) | `GET :uid/` | [docs](https://dash2.qryptal.com/docs/api2-api/#created-qr-code) |
