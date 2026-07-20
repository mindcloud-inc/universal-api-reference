# Find Nearby Stop Points with Transport for London

Finds nearby stop points in Transport for London.

## Endpoint

- **Method:** `GET`
- **Path:** `/StopPoint`
- **Base URL:** `https://api.tfl.gov.uk`
- **Official documentation:** [Find Nearby Stop Points](https://api.tfl.gov.uk/swagger/ui/index.html#!/StopPoint/StopPoint_GetByGeoPoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stopTypes` | query | `string` | yes | Comma-separated stop types to return. Valid values are available from StopPoint/Meta/StopTypes. |
| `lat` | query | `number` | yes | Latitude for the center of the search. |
| `lon` | query | `number` | yes | Longitude for the center of the search. |
| `radius` | query | `number` | no | Search radius in metres. TfL defaults this to 200 when omitted. |
