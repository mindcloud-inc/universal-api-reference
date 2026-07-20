# Get Address Logs with Blockscout

Retrieves logs emitted by or involving an address from Blockscout.

## Endpoint

- **Method:** `GET`
- **Path:** `/:chain_id/api/v2/addresses/:address_hash_param/logs`
- **Base URL:** `https://api.blockscout.com`
- **Official documentation:** [Get Address Logs](https://docs.blockscout.com/api-reference/get-address-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain_id` | path | `string` | no | Blockscout chain ID, for example 10 for Optimism. |
| `address_hash_param` | path | `string` | yes | Address hash to retrieve logs for. |
