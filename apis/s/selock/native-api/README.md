# Selock: Native API Reference

A consolidated summary of Selock's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://selock.co/en/docs/
- **API base URL:** `https://selock.co/api/v1`

## Authentication

### API Key

Use your Selock tenant token. MindCloud stores it as the implicit API key credential and sends it as the shared request body field `token`.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://selock.co/en/docs/selock-zapier-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Change Lock Status](actions/change-lock-status.md) | `POST /zaiper/change_lock_status/` | [docs](https://selock.co/en/docs/) |
| [Change Order](actions/change-order.md) | `POST /zaiper/change_order/` | [docs](https://selock.co/en/docs/) |
| [Create Order](actions/create-order.md) | `POST /zaiper/create_order/` | [docs](https://selock.co/en/docs/) |
| [List Categories](actions/list-categories.md) | `POST /get_data/` | [docs](https://selock.co/en/docs/) |
| [List Guests](actions/list-guests.md) | `POST /get_data/` | [docs](https://selock.co/en/docs/) |
| [List Locks](actions/list-locks.md) | `POST /get_data/` | [docs](https://selock.co/en/docs/) |
| [List Orders](actions/list-orders.md) | `POST /get_data/` | [docs](https://selock.co/en/docs/) |
| [List Rooms](actions/list-rooms.md) | `POST /get_data/` | [docs](https://selock.co/en/docs/) |
| [List Sources](actions/list-sources.md) | `POST /get_data/` | [docs](https://selock.co/en/docs/) |
| [List Statuses](actions/list-statuses.md) | `POST /get_data/` | [docs](https://selock.co/en/docs/) |
| [Subscribe Battery Alert](actions/subscribe-battery.md) | `POST /zaiper/subscribe/battery/` | [docs](https://selock.co/en/docs/selock-zapier-api/) |
| [Subscribe Lock Events](actions/subscribe-locks.md) | `POST /zaiper/subscribe/locks/` | [docs](https://selock.co/en/docs/selock-zapier-api/) |
| [Subscribe Lock Close Events](actions/subscribe-locks-close.md) | `POST /zaiper/subscribe/locks_close/` | [docs](https://selock.co/en/docs/selock-zapier-api/) |
| [Subscribe Lock Open Events](actions/subscribe-locks-open.md) | `POST /zaiper/subscribe/locks_open/` | [docs](https://selock.co/en/docs/selock-zapier-api/) |
| [Subscribe New Orders](actions/subscribe-orders.md) | `POST /zaiper/subscribe/orders/` | [docs](https://selock.co/en/docs/selock-zapier-api/) |
| [Subscribe Order Changes](actions/subscribe-orders-change.md) | `POST /zaiper/subscribe/orders_change/` | [docs](https://selock.co/en/docs/selock-zapier-api/) |
| [Unsubscribe Battery Alert](actions/unsubscribe-battery.md) | `POST /zaiper/unsubscribe/battery/` | [docs](https://selock.co/en/docs/selock-zapier-api/) |
| [Unsubscribe Lock Events](actions/unsubscribe-locks.md) | `POST /zaiper/unsubscribe/locks/` | [docs](https://selock.co/en/docs/selock-zapier-api/) |
| [Unsubscribe Lock Close Events](actions/unsubscribe-locks-close.md) | `POST /zaiper/unsubscribe/locks_close/` | [docs](https://selock.co/en/docs/selock-zapier-api/) |
| [Unsubscribe Lock Open Events](actions/unsubscribe-locks-open.md) | `POST /zaiper/unsubscribe/locks_open/` | [docs](https://selock.co/en/docs/selock-zapier-api/) |
| [Unsubscribe New Orders](actions/unsubscribe-orders.md) | `POST /zaiper/unsubscribe/orders/` | [docs](https://selock.co/en/docs/selock-zapier-api/) |
| [Unsubscribe Order Changes](actions/unsubscribe-orders-change.md) | `POST /zaiper/unsubscribe/orders_change/` | [docs](https://selock.co/en/docs/selock-zapier-api/) |
| [Verify Token](actions/verify-token.md) | `POST /zaiper/auth/` | [docs](https://selock.co/en/docs/selock-zapier-api/) |
