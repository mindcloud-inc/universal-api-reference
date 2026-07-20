# Get Earthquake By Event ID with USGS Earthquake Hazards

Finds an earthquake in USGS Earthquake Hazards by event ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/fdsnws/event/1/query`
- **Base URL:** `https://earthquake.usgs.gov`
- **Official documentation:** [Get Earthquake By Event ID](https://earthquake.usgs.gov/fdsnws/event/1/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventid` | query | `string` | yes | USGS event identifier to retrieve. |
