# Update Accommodation with Starfish

Updates an existing accommodation in Starfish.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accommodations/:accommodation_id`
- **Base URL:** `https://api.camping.care/v21`
- **Official documentation:** [Update Accommodation](https://documenter.getpostman.com/view/9467805/VUjQkj1d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accommodation_id` | path | `number` | yes | Accommodation ID. |
| `name` | query | `string` | no | Updated accommodation name. |
