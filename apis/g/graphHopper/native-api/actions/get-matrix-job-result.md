# Get Matrix Job Result with GraphHopper

Retrieves a matrix job result from GraphHopper.

## Endpoint

- **Method:** `GET`
- **Path:** `/matrix/solution/:jobId`
- **Base URL:** `https://graphhopper.com/api/1`
- **Official documentation:** [Get Matrix Job Result](https://docs.graphhopper.com/openapi/matrices/getmatrixsolutionjobid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Matrix computation job ID. |
