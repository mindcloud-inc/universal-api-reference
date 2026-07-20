# Planyo: Native API Reference

A consolidated summary of Planyo's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://www.planyo.com/api.php
- **API base URL:** `https://www.planyo.com/rest`

## Authentication

### API Key

Connect Planyo using an admin API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.planyo.com/api.php)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | query | `string` | no | Optional 2-letter ISO 639-1 language code such as EN or FR. |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Reservation Payment](actions/add-reservation-payment.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=add_reservation_payment) |
| [Add User](actions/add-user.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=add_user) |
| [Can Make Reservation](actions/can-make-reservation.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=can_make_reservation) |
| [Create Reservation](actions/create-reservation.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=make_reservation) |
| [Delete Reservation](actions/delete-reservation.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=delete_reservation) |
| [Do Reservation Action](actions/do-reservation-action.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=do_reservation_action) |
| [Get Event Times](actions/get-event-times.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=get_event_times) |
| [Get Rental Price](actions/get-rental-price.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=get_rental_price) |
| [Get Reservation Actions](actions/get-reservation-actions.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=get_reservation_actions) |
| [Get Reservation Data](actions/get-reservation-data.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=get_reservation_data) |
| [Get Reservation Payment Amount](actions/get-reservation-payment-amount.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=get_reservation_payment_amount) |
| [Get Resource Info](actions/get-resource-info.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=get_resource_info) |
| [Get Site Info](actions/get-site-info.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=get_site_info) |
| [Get User Data](actions/get-user-data.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=get_user_data) |
| [List Payments](actions/list-payments.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=list_payments) |
| [List Reservation Payments](actions/list-reservation-payments.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=list_reservation_payments) |
| [List Reservations](actions/list-reservations.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=list_reservations) |
| [List Resources](actions/list-resources.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=list_resources) |
| [List Users](actions/list-users.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=list_users) |
| [Remove Reservation Payment](actions/remove-reservation-payment.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=remove_reservation_payment) |
| [Search Reservations](actions/search-reservations.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=reservation_search) |
| [Update Reservation](actions/update-reservation.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=modify_reservation) |
| [Update Reservation Payment](actions/update-reservation-payment.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=modify_reservation_payment) |
| [Update User](actions/update-user.md) | `GET /` | [docs](https://www.planyo.com/api.php?topic=modify_user) |
