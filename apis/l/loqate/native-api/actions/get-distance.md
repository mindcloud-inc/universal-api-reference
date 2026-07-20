# Get Distance with Loqate

Retrieves the distance between locations from Loqate.

## Endpoint

- **Method:** `GET`
- **Path:** `/DistancesAndDirections/Interactive/Distance/v1.00/json6.ws`
- **Base URL:** `https://api.addressy.com`
- **Official documentation:** [Get Distance](https://docs.loqate.com/api-reference/geocode/distances-and-directions/distance)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Finish` | query | `string` | yes | The finish location or coordinates. |
| `Start` | query | `string` | yes | The start location or coordinates. |
