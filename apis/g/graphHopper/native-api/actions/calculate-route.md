# Calculate Route with GraphHopper

Calculates a route between points in GraphHopper.

## Endpoint

- **Method:** `POST`
- **Path:** `/route`
- **Base URL:** `https://graphhopper.com/api/1`
- **Official documentation:** [Calculate Route](https://docs.graphhopper.com/openapi/routing/postroute)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestBody` | body | `object` | yes | Route request JSON body matching GraphHopper's RouteRequest schema. |
