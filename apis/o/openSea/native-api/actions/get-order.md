# Get Order with OpenSea

Retrieves an order from OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/orders/chain/{chain}/protocol/{protocol_address}/{order_hash}`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Order](https://docs.opensea.io/reference/get_order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | The blockchain on which to filter the results |
| `protocol_address` | path | `string` | yes | Protocol contract address |
| `order_hash` | path | `string` | yes | Order hash |
