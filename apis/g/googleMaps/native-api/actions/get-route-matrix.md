# Get Route Matrix with Google Maps

## Endpoint

- **Method:** `POST`
- **Path:** `https://routes.googleapis.com/distanceMatrix/v2:computeRouteMatrix`
- **Official documentation:** [Get Route Matrix](https://developers.google.com/maps/documentation/routes/compute_route_matrix)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `destinations[].longitude` | body | `number` | no |
| `destinations[].latitude` | body | `number` | no |
| `origins[].latitude` | body | `number` | no |
| `origins[].routeModifiers.avoidTolls` | body | `boolean` | no |
| `origins[]` | body | `array` | no |
| `origins[].longitude` | body | `number` | no |
| `origins[].routeModifiers.avoidHighways` | body | `boolean` | no |
| `destinations[]` | body | `array` | no |
| `origins[].routeModifiers` | body | `object` | no |
| `origins[].routeModifiers.avoidFerries` | body | `boolean` | no |
| `origins[].routeModifiers.avoidIndoor` | body | `boolean` | no |
| `routingPreference` | body | `list` | no |
| `travelMode` | body | `list` | no |
