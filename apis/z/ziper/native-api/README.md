# Ziper: Native API Reference

A consolidated summary of Ziper's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/2881191/VUqmvyob
- **API base URL:** `https://ziper.io/api`

## Authentication

### API Key

Use the Ziper access token with an instance ID for query-parameter authentication.

### Credentials

- **API Key:** `apiKey` · required
- **Instance ID:** `instanceId` · required · Ziper WhatsApp instance ID from the WhatsApp Profiles page.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://ziper.io/whatsapp/get/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get QR Code](actions/get-qr-code.md) | `GET /getqrcode.php` | [docs](https://ziper.io/whatsapp/get/api) |
| [Send Buttons](actions/send-buttons.md) | `POST /send.php` | [docs](https://documenter.getpostman.com/view/2881191/VUqmvyob) |
| [Send List And Sections](actions/send-list-and-sections.md) | `POST /send.php` | [docs](https://documenter.getpostman.com/view/2881191/VUqmvyob) |
| [Send Location](actions/send-location.md) | `POST /send.php` | [docs](https://documenter.getpostman.com/view/2881191/VUqmvyob) |
| [Send Simple Text](actions/send-simple-text.md) | `POST /send.php` | [docs](https://documenter.getpostman.com/view/2881191/VUqmvyob) |
| [Send Template Buttons](actions/send-template-buttons.md) | `POST /send.php` | [docs](https://documenter.getpostman.com/view/2881191/VUqmvyob) |
| [Send VCard](actions/send-v-card.md) | `POST /send.php` | [docs](https://documenter.getpostman.com/view/2881191/VUqmvyob) |
