# Get Addresses with Blockscout

Retrieves native coin holders from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/addresses`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Addresses](https://docs.blockscout.com/api-reference/get-native-coin-holders-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | Blockscout chain ID, for example 10 for Optimism. |
