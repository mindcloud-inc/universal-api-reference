# List Places with Starfish

Retrieves places for a specific accommodation in Starfish.

## Endpoint

- **Method:** `GET`
- **Path:** `/accommodations/:accommodation_id/places`
- **Base URL:** `https://api.camping.care/v21`
- **Official documentation:** [List Places](https://documenter.getpostman.com/view/9467805/VUjQkj1d)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accommodation_id` | path | `number` | yes | Accommodation ID. |
