# Get Smart Contracts with Blockscout

Retrieves verified smart contracts from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/smart-contracts/`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Smart Contracts](https://docs.blockscout.com/api-reference/get-verified-smart-contracts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | Blockscout chain ID, for example 10 for Optimism. |
