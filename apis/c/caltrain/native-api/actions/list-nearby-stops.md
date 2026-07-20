# List Nearby Stops with Caltrain

Finds Caltrain stops near a location.

## Endpoint

- **Method:** `GET`
- **Path:** `/gtfs/stops/nearby/:longitude/:latitude/:radius`
- **Base URL:** `https://www.caltrain.com`
- **Official documentation:** [List Nearby Stops](https://www.caltrain.com/developer-resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `longitude` | path | `number` | yes | Longitude near the target stop search area. |
| `latitude` | path | `number` | yes | Latitude near the target stop search area. |
| `radius` | path | `number` | yes | Search radius in miles. |
