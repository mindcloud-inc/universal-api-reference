# BoothBook: Native API Reference

A consolidated summary of BoothBook's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://v1-support.boothbook.com/article/developer-api-overview
- **API base URL:** `https://mindcloud.boothbook.com`

## Authentication

### Custom Key + Secret

BoothBook requests require two explicit form fields: key and secret. Use this auth entry to send both values without the platform's default bearer header.

### Credentials

- **Client Key:** `key` · required · BoothBook client key from the Developer page.
- **Secret Key:** `secret` · required · BoothBook secret key from the Developer page.

[Official authentication documentation](https://v1-support.boothbook.com/article/accessing-your-boothbook-api-keys)

## API conventions

Request bodies use multipart form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | `POST /api/v1/get/account` | [docs](https://v1-support.boothbook.com/article/endpoint-account) |
| [List Bookings](actions/list-bookings.md) | `POST /api/v1/get/bookings` | [docs](https://v1-support.boothbook.com/article/endpoint-bookings) |
