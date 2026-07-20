# Solve Clustering Problem with GraphHopper

Solves a clustering problem in GraphHopper.

## Endpoint

- **Method:** `POST`
- **Path:** `/cluster`
- **Base URL:** `https://graphhopper.com/api/1`
- **Official documentation:** [Solve Clustering Problem](https://docs.graphhopper.com/openapi/clustering/postcluster)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestBody` | body | `object` | yes | Clustering request JSON body matching GraphHopper's ClusterRequest schema. |
