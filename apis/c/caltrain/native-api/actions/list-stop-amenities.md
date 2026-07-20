# List Stop Amenities with Caltrain

Retrieves amenities for a Caltrain stop.

## Endpoint

- **Method:** `GET`
- **Path:** `/gtfs/stops/:stopId/amenities`
- **Base URL:** `https://www.caltrain.com`
- **Official documentation:** [List Stop Amenities](https://www.caltrain.com/developer-resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stopId` | path | `string` | yes | Caltrain stop identifier such as 70021 or 22nd_street. |
