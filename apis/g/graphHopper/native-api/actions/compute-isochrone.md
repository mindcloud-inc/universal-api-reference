# Compute Isochrone with GraphHopper

Computes an isochrone map in GraphHopper.

## Endpoint

- **Method:** `GET`
- **Path:** `/isochrone`
- **Base URL:** `https://graphhopper.com/api/1`
- **Official documentation:** [Compute Isochrone](https://docs.graphhopper.com/openapi/isochrones/getisochrone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `point` | query | `string` | yes | Center point as `lat,lon`. |
| `profile` | query | `string` | yes | Routing profile such as `car`, `bike`, or `foot`. |
| `time_limit` | query | `number` | no | Travel time limit in seconds. |
| `distance_limit` | query | `number` | no | Travel distance limit in meters. |
| `buckets` | query | `number` | no | Number of isochrone buckets. |
