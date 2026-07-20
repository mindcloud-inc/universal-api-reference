# Match GPX Trace with GraphHopper

Matches a GPX trace in GraphHopper.

## Endpoint

- **Method:** `POST`
- **Path:** `/match`
- **Base URL:** `https://graphhopper.com/api/1`
- **Official documentation:** [Match GPX Trace](https://docs.graphhopper.com/openapi/map-matching/postmatch)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/gpx+xml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gpx` | body | `string` | yes | GPX XML content to map-match. |
| `profile` | query | `string` | yes | Routing profile for map matching. |
| `gps_accuracy` | query | `number` | no | GPS accuracy in meters. |
| `locale` | query | `string` | no | Locale of instructions. |
| `instructions` | query | `boolean` | no | Whether turn-by-turn instructions should be calculated. |
| `points_encoded` | query | `boolean` | no | Whether returned geometry should use encoded polyline format. |
