# Solve Route Optimization Problem with GraphHopper

Solves a route optimization problem in GraphHopper.

## Endpoint

- **Method:** `POST`
- **Path:** `/vrp`
- **Base URL:** `https://graphhopper.com/api/1`
- **Official documentation:** [Solve Route Optimization Problem](https://docs.graphhopper.com/openapi/route-optimization/postvrp)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestBody` | body | `object` | yes | Route optimization request JSON body matching GraphHopper's Request schema. |
