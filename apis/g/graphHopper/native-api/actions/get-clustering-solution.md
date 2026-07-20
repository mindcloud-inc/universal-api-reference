# Get Clustering Solution with GraphHopper

Retrieves a clustering solution from GraphHopper.

## Endpoint

- **Method:** `GET`
- **Path:** `/cluster/solution/:jobId`
- **Base URL:** `https://graphhopper.com/api/1`
- **Official documentation:** [Get Clustering Solution](https://docs.graphhopper.com/openapi/clustering/getclustersolutionjobid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Clustering job ID. |
