# KlipLink: Native API Reference

A consolidated summary of KlipLink's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.klipl.ink/api/overview
- **API base URL:** `https://api.klipl.ink`

## Authentication

### API Key

Use a KlipLink API key sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.klipl.ink/api/authentication)

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Link](actions/create-link.md) | `POST /v1/links` | [docs](https://docs.klipl.ink/api/links/create-link) |
| [Create QR Code](actions/create-qr-code.md) | `POST /v1/qrcodes` | [docs](https://docs.klipl.ink/api/qrcodes/create-qrcode) |
| [Delete Link](actions/delete-link.md) | `DELETE /v1/links/:short_url` | [docs](https://docs.klipl.ink/api/links/delete-link) |
| [Delete QR Code](actions/delete-qr-code.md) | `DELETE /v1/qrcodes/:short_url` | [docs](https://docs.klipl.ink/api/qrcodes/delete-qrcode) |
| [Get Link](actions/get-link.md) | `GET /v1/links/:short_url` | [docs](https://docs.klipl.ink/api/links/get-a-link) |
| [Get QR Code](actions/get-qr-code.md) | `GET /v1/qrcodes/:short_url` | [docs](https://docs.klipl.ink/api/qrcodes/get-a-qrcode) |
| [List Domains](actions/list-domains.md) | `GET /v1/domains` | [docs](https://docs.klipl.ink/api/domains/get-all-domains) |
| [List Links](actions/list-links.md) | `GET /v1/links` | [docs](https://docs.klipl.ink/api/links/get-all-links) |
| [List QR Codes](actions/list-qr-codes.md) | `GET /v1/qrcodes` | [docs](https://docs.klipl.ink/api/qrcodes/get-all-qrcodes) |
| [Update Link](actions/update-link.md) | `PUT /v1/links/:short_url` | [docs](https://docs.klipl.ink/api/links/update-link) |
| [Update QR Code](actions/update-qr-code.md) | `PUT /v1/qrcodes/:short_url` | [docs](https://docs.klipl.ink/api/qrcodes/update-qrcode) |
