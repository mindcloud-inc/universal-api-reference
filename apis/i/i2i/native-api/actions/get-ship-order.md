# Get ship order with i2i

Retrieves a ship order from i2i by order ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/ibis/api/v1.1/customers/{consumerTag}/ship/orders/:orderId`
- **Base URL:** `https://exch.i2i.ca`
- **Official documentation:** [Get ship order](https://www.i2i.ca/why-i2i/our-software)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | i2i ship order ID to fetch. |
