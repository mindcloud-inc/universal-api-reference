# Create Listing with OpenSea

Creates a listing in OpenSea.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/orders/{chain}/{protocol}/listings`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Create Listing](https://docs.opensea.io/reference/post_listing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | The blockchain on which to filter the results |
| `protocol` | path | `string` | yes | — |
| `parameters` | body | `object` | yes | — |
| `protocol_address` | body | `string` | yes | — |
| `signature` | body | `string` | yes | — |
