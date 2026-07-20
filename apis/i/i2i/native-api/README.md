# i2i: Native API Reference

A consolidated summary of i2i's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://www.i2i.ca/why-i2i/our-software
- **API base URL:** `https://exch.i2i.ca`

## Authentication

### i2i HMAC API key

Uses the i2i API key as the HMAC SHA-256 signing secret. Requests are signed with X-Echo-Signature and X-Echo-User headers; the default bearer Authorization header is removed by the request mapper.

### Credentials

- **API Key:** `apiKey` · required
- **Username:** `username` · required · i2i username used in the X-Echo-User signing header.
- **Consumer tag:** `consumerTag` · required · i2i customer/consumer tag used in the ship order URL path.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.i2i.ca/why-i2i/our-software)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `page_info` in the query string as the pagination cursor.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create order](actions/create-order.md) | `POST /ibis/api/v1.1/customers/{{credentials.consumerTag}}/ship/orders` | [docs](https://www.i2i.ca/why-i2i/our-software) |
| [Get ship order](actions/get-ship-order.md) | `GET /ibis/api/v1.1/customers/{{credentials.consumerTag}}/ship/orders/:orderId` | [docs](https://www.i2i.ca/why-i2i/our-software) |
| [List ship orders](actions/list-ship-orders.md) | `GET /ibis/api/v1.3/customers/{{credentials.consumerTag}}/ship/orders` | [docs](https://www.i2i.ca/why-i2i/our-software) |
