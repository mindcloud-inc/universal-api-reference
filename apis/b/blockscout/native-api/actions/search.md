# Search with Blockscout

Finds matching addresses, blocks, transactions, tokens, and domains in Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/search`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Search](https://docs.blockscout.com/api-reference/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | Blockscout chain ID, for example 10 for Optimism. |
| `q` | query | `string` | yes | Search query. |
