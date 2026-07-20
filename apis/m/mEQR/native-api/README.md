# ME-QR: Native API Reference

A consolidated summary of ME-QR's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://me-qr.com/api/doc
- **API base URL:** `https://me-qr.com`

## Authentication

### API Key

Use your ME-QR API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-AUTH-TOKEN: <apiKey>
```

[Official authentication documentation](https://me-qr.com/api/doc)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Email QR](actions/create-email-qr.md) | `POST /api/v2/qr/email/create` | [docs](https://me-qr.com/api/doc) |
| [Create File QR](actions/create-file-qr.md) | `POST /api/v2/qr/file/create` | [docs](https://me-qr.com/api/doc) |
| [Create Gallery QR](actions/create-gallery-qr.md) | `POST /api/v2/qr/gallery/create` | [docs](https://me-qr.com/api/doc) |
| [Create Link List QR](actions/create-link-list-qr.md) | `POST /api/v2/qr/link-list/create` | [docs](https://me-qr.com/api/doc) |
| [Create Link QR](actions/create-link-qr.md) | `POST /api/v2/qr/link/create` | [docs](https://me-qr.com/api/doc) |
| [Create Map QR](actions/create-map-qr.md) | `POST /api/v2/qr/map/create` | [docs](https://me-qr.com/api/doc) |
| [Create PDF QR](actions/create-pdfqr.md) | `POST /api/v2/qr/pdf/create` | [docs](https://me-qr.com/api/doc) |
| [Create Phone QR](actions/create-phone-qr.md) | `POST /api/v2/qr/phone/create` | [docs](https://me-qr.com/api/doc) |
| [Create Text QR](actions/create-text-qr.md) | `POST /api/v2/qr/text/create` | [docs](https://me-qr.com/api/doc) |
| [Create vCard QR](actions/create-v-card-qr.md) | `POST /api/v2/qr/vcard/create` | [docs](https://me-qr.com/api/doc) |
| [Create Video QR](actions/create-video-qr.md) | `POST /api/v2/qr/video/create` | [docs](https://me-qr.com/api/doc) |
| [Create WhatsApp QR](actions/create-whats-app-qr.md) | `POST /api/v2/qr/whatsapp/create` | [docs](https://me-qr.com/api/doc) |
| [Create WiFi QR](actions/create-wi-fi-qr.md) | `POST /api/v2/qr/wifi/create` | [docs](https://me-qr.com/api/doc) |
| [Get Email QR](actions/get-email-qr.md) | `GET /api/v2/qr/email/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Get File QR](actions/get-file-qr.md) | `GET /api/v2/qr/file/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Get Gallery QR](actions/get-gallery-qr.md) | `GET /api/v2/qr/gallery/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Get Link List QR](actions/get-link-list-qr.md) | `GET /api/v2/qr/link-list/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Get Link QR](actions/get-link-qr.md) | `GET /api/v2/qr/link/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Get Map QR](actions/get-map-qr.md) | `GET /api/v2/qr/map/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Get PDF QR](actions/get-pdfqr.md) | `GET /api/v2/qr/pdf/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Get Phone QR](actions/get-phone-qr.md) | `GET /api/v2/qr/phone/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Get Text QR](actions/get-text-qr.md) | `GET /api/v2/qr/text/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Get vCard QR](actions/get-v-card-qr.md) | `GET /api/v2/qr/vcard/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Get Video QR](actions/get-video-qr.md) | `GET /api/v2/qr/video/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Get WhatsApp QR](actions/get-whats-app-qr.md) | `GET /api/v2/qr/whatsapp/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Get WiFi QR](actions/get-wi-fi-qr.md) | `GET /api/v2/qr/wifi/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [List QRs](actions/list-q-rs.md) | `GET /api/qr/list/` | [docs](https://me-qr.com/api/doc) |
| [Update Email QR](actions/update-email-qr.md) | `PUT /api/v2/qr/email/update/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Update File QR](actions/update-file-qr.md) | `PUT /api/v2/qr/file/update/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Update Gallery QR](actions/update-gallery-qr.md) | `PUT /api/v2/qr/gallery/update/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Update Link List QR](actions/update-link-list-qr.md) | `PUT /api/v2/qr/link-list/update/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Update Link QR](actions/update-link-qr.md) | `PUT /api/v2/qr/link/update/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Update Map QR](actions/update-map-qr.md) | `PUT /api/v2/qr/map/update/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Update PDF QR](actions/update-pdfqr.md) | `PUT /api/v2/qr/pdf/update/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Update Phone QR](actions/update-phone-qr.md) | `PUT /api/v2/qr/phone/update/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Update Text QR](actions/update-text-qr.md) | `PUT /api/v2/qr/text/update/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Update vCard QR](actions/update-v-card-qr.md) | `PUT /api/v2/qr/vcard/update/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Update Video QR](actions/update-video-qr.md) | `PUT /api/v2/qr/video/update/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Update WhatsApp QR](actions/update-whats-app-qr.md) | `PUT /api/v2/qr/whatsapp/update/:entryUID` | [docs](https://me-qr.com/api/doc) |
| [Update WiFi QR](actions/update-wi-fi-qr.md) | `PUT /api/v2/qr/wifi/update/:entryUID` | [docs](https://me-qr.com/api/doc) |
