# Get Payment Token Details with OpenSea

Retrieves a payment token from OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/chain/{chain}/payment_token/{address}`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Payment Token Details](https://docs.opensea.io/reference/get_payment_token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | path | `string` | yes | The unique public blockchain identifier for the contract |
| `chain` | path | `string` | yes | The blockchain on which to filter the results |
