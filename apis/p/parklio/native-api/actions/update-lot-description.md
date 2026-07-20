# Update Lot Description with Parklio

Updates a lot description in Parklio.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/lots/:id`
- **Base URL:** `https://api.parklio.com`
- **Official documentation:** [Update Lot Description](https://api.parklio.com/api#/LOTS/LotsController_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Parklio lot ID. |
| `description` | body | `string` | yes | The new lot description to apply. |
