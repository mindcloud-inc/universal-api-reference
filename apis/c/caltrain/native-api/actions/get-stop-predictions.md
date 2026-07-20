# Get Stop Predictions with Caltrain

Retrieves arrival predictions for a Caltrain stop.

## Endpoint

- **Method:** `GET`
- **Path:** `/gtfs/stops/:stopId/predictions`
- **Base URL:** `https://www.caltrain.com`
- **Official documentation:** [Get Stop Predictions](https://www.caltrain.com/developer-resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stopId` | path | `string` | yes | Caltrain parent stop identifier such as 22nd_street. |
