# List Charging Locations Along Route with Open Charge Map

## Endpoint

- **Method:** `GET`
- **Path:** `/poi`
- **Base URL:** `https://api.openchargemap.io/v3`
- **Official documentation:** [List Charging Locations Along Route](https://www.openchargemap.org/develop/api#/operations/get-poi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `polyline` | query | `string` | yes | Encoded route polyline. Use with distance to search along a route. |
| `distance` | query | `number` | yes | Search distance around the route polyline. |
| `distanceunit` | query | `list` | yes | Distance unit: miles or km. Accepted values: `0`, `1`. |
