# Accept Dispute with OPN

Accepts an existing dispute in OPN.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/disputes/:id/accept`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [Accept Dispute](https://docs.omise.co/disputes-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The dispute ID to accept. |
