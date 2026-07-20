# List ship orders with i2i

Retrieves ship orders from i2i by status and date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/ibis/api/v1.3/customers/{consumerTag}/ship/orders`
- **Base URL:** `https://exch.i2i.ca`
- **Official documentation:** [List ship orders](https://www.i2i.ca/why-i2i/our-software)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `st` | query | `string` | no | Earliest ship-order timestamp accepted by i2i for this lookup. |
| `et` | query | `string` | no | Latest ship-order timestamp accepted by i2i for this lookup. |
| `status` | query | `string` | no | Ship order status filter. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `complete` | query | `list` | no | Completion flag filter used by i2i. Accepted values: `0`, `1`. |
