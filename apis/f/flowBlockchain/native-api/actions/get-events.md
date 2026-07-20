# Get Events with Flow Blockchain

Retrieves events from Flow Blockchain.

## Endpoint

- **Method:** `GET`
- **Path:** `/events`
- **Base URL:** `https://rest-mainnet.onflow.org/v1`
- **API:** rest
- **Official documentation:** [Get Events](https://developers.flow.com/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_height` | query | `string` | no | End block height for event search. |
| `start_height` | query | `string` | no | Start block height for event search. |
| `type` | query | `string` | yes | Fully qualified Flow event type. |
