# Get Contract with OpenSea

Retrieves a contract from OpenSea.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/chain/{chain}/contract/{address}`
- **Base URL:** `https://api.opensea.io`
- **Official documentation:** [Get Contract](https://docs.opensea.io/reference/get_contract)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | path | `string` | yes | The unique public blockchain identifier for the contract |
| `chain` | path | `string` | yes | The blockchain on which to filter the results |
