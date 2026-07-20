# Get Order with Big Cartel

Retrieves an order from Big Cartel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/[:account-id]/orders/[:order-id]`
- **Base URL:** `https://api.bigcartel.com`
- **Official documentation:** [Get Order](https://developers.bigcartel.com/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `number` | yes | The Big Cartel account ID. |
| `order-id` | path | `string` | yes | Order identifier from the orders endpoint. |
