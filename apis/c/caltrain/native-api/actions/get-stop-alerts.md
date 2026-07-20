# Get Stop Alerts with Caltrain

Retrieves alerts for a Caltrain stop.

## Endpoint

- **Method:** `GET`
- **Path:** `/gtfs/stops/:stopId/alerts`
- **Base URL:** `https://www.caltrain.com`
- **Official documentation:** [Get Stop Alerts](https://www.caltrain.com/developer-resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stopId` | path | `string` | yes | Caltrain stop identifier such as 22nd_street. |
