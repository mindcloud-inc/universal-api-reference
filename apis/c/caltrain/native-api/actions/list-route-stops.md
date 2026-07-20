# List Route Stops with Caltrain

Retrieves stops for a Caltrain route.

## Endpoint

- **Method:** `GET`
- **Path:** `/gtfs/routes/:routeId/stops`
- **Base URL:** `https://www.caltrain.com`
- **Official documentation:** [List Route Stops](https://www.caltrain.com/developer-resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `routeId` | path | `string` | yes | Caltrain route identifier such as Limited or Express. |
