# Get Token Details Catalog with OpenSea

Retrieves a token from OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/chain/{chain}/token/{address}`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Token Details Catalog](https://docs.opensea.io/reference/get_token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | path | `string` | yes | The blockchain on which to filter the results |
| `address` | path | `string` | yes | The contract address of the token |
