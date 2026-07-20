# Cancel Order with OTO

Cancels an existing order in OTO.

## Endpoint

- **Method:** `POST`
- **Path:** `/cancelOrder`
- **Base URL:** `https://api.tryoto.com/rest/v2`
- **Official documentation:** [Cancel Order](https://help.tryoto.com/en/support/solutions/articles/150000213808-orders-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | body | `string` | yes | The merchant order identifier to cancel. |
