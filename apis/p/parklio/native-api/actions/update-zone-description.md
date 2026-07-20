# Update Zone Description with Parklio

Updates a zone description in Parklio.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/zones/:id`
- **Base URL:** `https://api.parklio.com`
- **Official documentation:** [Update Zone Description](https://api.parklio.com/api#/ZONES/ZonesController_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Parklio zone ID. |
| `description` | body | `string` | yes | The new zone description to apply. |
