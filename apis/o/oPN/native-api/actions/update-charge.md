# Update Charge with OPN

Updates an existing charge in OPN.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/charges/:id`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [Update Charge](https://docs.omise.co/charge-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The updated charge description. |
| `id` | path | `string` | yes | The charge ID to update. |
