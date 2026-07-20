# List GeoJSON Event Features for Event with EONET

Retrieves GeoJSON event features for an event from EONET.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/geojson`
- **Base URL:** `https://eonet.gsfc.nasa.gov/api/v3`
- **Official documentation:** [List GeoJSON Event Features for Event](https://eonet.gsfc.nasa.gov/docs/v3#events-api-geojson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | Unique EONET event ID. |
