# Cancel Order with OpenSea

Cancels an order in OpenSea.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/orders/chain/{chain}/protocol/{protocol_address}/{order_hash}/cancel`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Cancel Order](https://docs.opensea.io/reference/cancel_order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | The blockchain on which to filter the results |
| `protocol_address` | path | `string` | yes | — |
| `order_hash` | path | `string` | yes | — |
| `offererSignature` | body | `string` | no | — |
