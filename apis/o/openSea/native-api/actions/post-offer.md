# Create Item Offer with OpenSea

Creates an item offer in OpenSea.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/orders/{chain}/{protocol}/offers`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Create Item Offer](https://docs.opensea.io/reference/post_offer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | The blockchain on which to filter the results |
| `protocol` | path | `string` | yes | — |
| `parameters` | body | `object` | yes | — |
| `protocol_address` | body | `string` | yes | — |
| `signature` | body | `string` | yes | — |
