# QR Api: Native API Reference

A consolidated summary of QR Api's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://qrapi.io/api-documentation/
- **OpenAPI specification:** https://qrapi.io/api-documentation/swagger-ui-init.js
- **API base URL:** `https://qrapi.io/v2`

## Authentication

### API Key

Authenticate requests with the QR Api API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.qrapi.io/hc/en-us/articles/33944207638681-How-do-I-find-my-API-Key)

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Email QR Code](actions/create-email-qr-code.md) | `GET /qrcode/email` | [docs](https://qrapi.io/api-documentation/) |
| [Create Google Maps QR Code](actions/create-google-maps-qr-code.md) | `GET /qrcode/googlemaps` | [docs](https://qrapi.io/api-documentation/) |
| [Create Phone Call QR Code](actions/create-phone-call-qr-code.md) | `GET /qrcode/phonecall` | [docs](https://qrapi.io/api-documentation/) |
| [Create SMS QR Code](actions/create-sms-qr-code.md) | `GET /qrcode/SMS` | [docs](https://qrapi.io/api-documentation/) |
| [Create Text QR Code](actions/create-text-qr-code.md) | `GET /qrcode/text` | [docs](https://qrapi.io/api-documentation/) |
| [Create URL QR Code](actions/create-url-qr-code.md) | `GET /qrcode/url` | [docs](https://qrapi.io/api-documentation/) |
| [Create VCard QR Code](actions/create-vcard-qr-code.md) | `GET /qrcode/vcard` | [docs](https://qrapi.io/api-documentation/) |
| [Create WiFi QR Code](actions/create-wifi-qr-code.md) | `GET /qrcode/wifi` | [docs](https://qrapi.io/api-documentation/) |
