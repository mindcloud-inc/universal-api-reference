# Find Nearby Airports with Airlabs

Finds nearby airports in Airlabs by coordinates.

## Endpoint

- **Method:** `GET`
- **Path:** `/nearby`
- **Base URL:** `https://airlabs.co/api/v9`
- **Official documentation:** [Find Nearby Airports](https://airlabs.co/docs/nearby)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lat` | query | `number` | yes | Geo-location latitude. |
| `lng` | query | `number` | yes | Geo-location longitude. |
| `distance` | query | `number` | yes | Distance from the location in kilometers. |
