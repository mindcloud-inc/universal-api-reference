# Get Order Details with OTO

Retrieves order details from the OTO API.

## Endpoint

- **Method:** `GET`
- **Path:** `/orderDetails`
- **Base URL:** `https://api.tryoto.com/rest/v2`
- **Official documentation:** [Get Order Details](https://help.tryoto.com/en/support/solutions/articles/150000213808-orders-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | query | `string` | yes | The merchant order identifier to fetch. |
