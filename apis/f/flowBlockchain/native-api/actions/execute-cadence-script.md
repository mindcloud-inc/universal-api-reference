# Execute Cadence Script with Flow Blockchain

Executes a Cadence script on Flow Blockchain.

## Endpoint

- **Method:** `POST`
- **Path:** `/scripts`
- **Base URL:** `https://rest-mainnet.onflow.org/v1`
- **API:** rest
- **Official documentation:** [Execute Cadence Script](https://developers.flow.com/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `arguments[]` | body | `array<string>` | no | Cadence arguments encoded as Base64 JSON-Cadence values. |
| `block_height` | query | `string` | no | Optional block height to execute the script against. Incompatible with block ID. |
| `block_id` | query | `string` | no | Optional block ID to execute the script against. |
| `script` | body | `string` | yes | Base64-encoded Cadence script to execute. |
