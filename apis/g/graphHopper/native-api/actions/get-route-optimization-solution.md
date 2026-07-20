# Get Route Optimization Solution with GraphHopper

Retrieves a route optimization solution from GraphHopper.

## Endpoint

- **Method:** `GET`
- **Path:** `/vrp/solution/:jobId`
- **Base URL:** `https://graphhopper.com/api/1`
- **Official documentation:** [Get Route Optimization Solution](https://docs.graphhopper.com/openapi/route-optimization/getvrpsolutionjobid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Route optimization job ID. |
