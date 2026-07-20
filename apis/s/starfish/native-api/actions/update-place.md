# Update Place with Starfish

Updates an existing place in a Starfish accommodation.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accommodations/:accommodation_id/places/:place_id`
- **Base URL:** `https://api.camping.care/v21`
- **Official documentation:** [Update Place](https://documenter.getpostman.com/view/9467805/VUjQkj1d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accommodation_id` | path | `number` | yes | Accommodation ID. |
| `place_id` | path | `number` | yes | Place ID. |
| `latitude` | query | `number` | no | Updated place latitude. |
| `longitude` | query | `number` | no | Updated place longitude. |
