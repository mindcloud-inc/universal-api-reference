# Close Dispute with OPN

Closes an existing dispute in OPN.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/disputes/:id/close`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [Close Dispute](https://docs.omise.co/disputes-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The dispute ID to close. |
| `status` | body | `string` | no | How to close the dispute: won or lost. |
