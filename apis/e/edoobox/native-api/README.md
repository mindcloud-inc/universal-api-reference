# Edoobox: Native API Reference

A consolidated summary of Edoobox's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.docs.edoobox.com/
- **API base URL:** `https://app2.edoobox.com/v2`

## Authentication

### JWT Token + EDID

Use a generated edoobox JWT access token together with the matching EDID returned by the auth endpoint.

### Credentials

- **Access Token:** `accessToken` · required · The JWT access token returned by the edoobox auth endpoint.
- **EDID:** `edid` · required · The current edoobox account edid returned alongside the JWT access token.

Send these headers with each API request:

```http
edid: <edid>
Authorization: Bearer <accessToken>
```

[Official authentication documentation](https://v2.docs.edoobox.com/en/docs/edoobox-api-erste-schritte)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Booking](actions/cancel-booking.md) | `PUT /booking/:booking_id/cancel` | [docs](https://api.docs.edoobox.com/) |
| [Copy Offer](actions/copy-offer.md) | `POST /offer/:offer_id/copy` | [docs](https://api.docs.edoobox.com/) |
| [Create Booking](actions/create-booking.md) | `POST /booking` | [docs](https://api.docs.edoobox.com/) |
| [Create Category](actions/create-category.md) | `POST /category` | [docs](https://api.docs.edoobox.com/) |
| [Create Invoice](actions/create-invoice.md) | `POST /invoice` | [docs](https://api.docs.edoobox.com/) |
| [Create Note](actions/create-note.md) | `POST /note` | [docs](https://api.docs.edoobox.com/) |
| [Create Offer](actions/create-offer.md) | `POST /offer` | [docs](https://api.docs.edoobox.com/) |
| [Create User](actions/create-user.md) | `POST /user` | [docs](https://api.docs.edoobox.com/) |
| [Delete Category](actions/delete-category.md) | `DELETE /category/:category_id` | [docs](https://api.docs.edoobox.com/) |
| [Delete Offer](actions/delete-offer.md) | `DELETE /offer/:offer_id` | [docs](https://api.docs.edoobox.com/) |
| [Delete User](actions/delete-user.md) | `DELETE /user/:user_id` | [docs](https://api.docs.edoobox.com/) |
| [Get Booking](actions/get-booking.md) | `GET /booking/:booking_id` | [docs](https://api.docs.edoobox.com/) |
| [Get Category](actions/get-category.md) | `GET /category/:category_id` | [docs](https://api.docs.edoobox.com/) |
| [Get Category Dashboard](actions/get-category-dashboard.md) | `GET /category/:category_id/dashboard` | [docs](https://api.docs.edoobox.com/) |
| [Get Invoice](actions/get-invoice.md) | `GET /invoice/:id` | [docs](https://api.docs.edoobox.com/) |
| [Get Offer](actions/get-offer.md) | `GET /offer/:offer_id` | [docs](https://api.docs.edoobox.com/) |
| [Get User](actions/get-user.md) | `GET /user/:user_id` | [docs](https://api.docs.edoobox.com/) |
| [Get User Dashboard](actions/get-user-dashboard.md) | `GET /user/:user_id/dashboard` | [docs](https://api.docs.edoobox.com/) |
| [Get Vat](actions/get-vat.md) | `GET /vat/:vat_id` | [docs](https://api.docs.edoobox.com/) |
| [List Bookings](actions/list-bookings.md) | `GET /booking/list` | [docs](https://api.docs.edoobox.com/) |
| [List Categories](actions/list-categories.md) | `GET /category/list` | [docs](https://api.docs.edoobox.com/) |
| [List Invoices](actions/list-invoices.md) | `GET /invoice/list` | [docs](https://api.docs.edoobox.com/) |
| [List Notes](actions/list-notes.md) | `GET /note/list` | [docs](https://api.docs.edoobox.com/) |
| [List Offers](actions/list-offers.md) | `GET /offer/list` | [docs](https://api.docs.edoobox.com/) |
| [List Transactions](actions/list-transactions.md) | `GET /transaction/list` | [docs](https://api.docs.edoobox.com/) |
| [List Users](actions/list-users.md) | `GET /user/list` | [docs](https://api.docs.edoobox.com/) |
| [List Vats](actions/list-vats.md) | `GET /vat/list` | [docs](https://api.docs.edoobox.com/) |
| [Update Category](actions/update-category.md) | `PUT /category/:category_id` | [docs](https://api.docs.edoobox.com/) |
| [Update Offer](actions/update-offer.md) | `PUT /offer/:offer_id` | [docs](https://api.docs.edoobox.com/) |
| [Update User](actions/update-user.md) | `PUT /user/:user_id` | [docs](https://api.docs.edoobox.com/) |
