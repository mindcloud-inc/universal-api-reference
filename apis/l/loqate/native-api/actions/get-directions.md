# Get Directions with Loqate

Retrieves directions between locations from Loqate.

## Endpoint

- **Method:** `GET`
- **Path:** `/DistancesAndDirections/Interactive/Directions/v2.00/json6.ws`
- **Base URL:** `https://api.addressy.com`
- **Official documentation:** [Get Directions](https://docs.loqate.com/api-reference/geocode/distances-and-directions/directions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Finish` | query | `string` | yes | The finish location or coordinates. |
| `Start` | query | `string` | yes | The start location or coordinates. |
