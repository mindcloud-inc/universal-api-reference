# Submit Signed Transaction with Flow Blockchain

Submits a signed transaction to Flow Blockchain.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions`
- **Base URL:** `https://rest-mainnet.onflow.org/v1`
- **API:** rest
- **Official documentation:** [Submit Signed Transaction](https://developers.flow.com/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `arguments[]` | body | `array<string>` | yes | Array of Base64-encoded JSON-Cadence transaction arguments. |
| `authorizers[]` | body | `array<string>` | yes | Flow addresses authorizing the transaction. |
| `envelope_signatures[]` | body | `array<object>` | yes | Envelope signature objects for the already-signed transaction. |
| `gas_limit` | body | `string` | yes | Maximum computation units allowed for the transaction. |
| `payer` | body | `string` | yes | Flow address paying transaction fees. |
| `payload_signatures[]` | body | `array<object>` | yes | Payload signature objects for the already-signed transaction. |
| `proposal_key` | body | `object` | yes | Proposal key object with address, key index, and sequence number. |
| `reference_block_id` | body | `string` | yes | Reference block ID for the signed transaction. |
| `script` | body | `string` | yes | Base64-encoded Cadence transaction script. |
