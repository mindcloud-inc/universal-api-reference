# Get Intent with Privy

Retrieves an intent from Privy by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/intents/{{intentId}}`
- **Base URL:** `https://api.privy.io`
- **Official documentation:** [Get Intent](https://api.privy.io/v1/openapi.json#/paths/~1v1~1intents~1{intent_id}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `intent_id` | path | `string` | yes | Privy intent ID. |
