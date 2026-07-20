# Update Dispute with OPN

Updates an existing dispute in OPN.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/disputes/:id`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [Update Dispute](https://docs.omise.co/disputes-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The dispute ID to update. |
| `message` | body | `string` | no | The dispute response message. |
