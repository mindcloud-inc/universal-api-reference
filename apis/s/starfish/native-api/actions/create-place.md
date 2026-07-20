# Create Place with Starfish

Creates a new place in a Starfish accommodation.

## Endpoint

- **Method:** `POST`
- **Path:** `/accommodations/:accommodation_id/places`
- **Base URL:** `https://api.camping.care/v21`
- **Official documentation:** [Create Place](https://documenter.getpostman.com/view/9467805/VUjQkj1d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accommodation_id` | path | `number` | yes | Parent accommodation ID. |
| `name` | query | `string` | no | Optional place name. |
