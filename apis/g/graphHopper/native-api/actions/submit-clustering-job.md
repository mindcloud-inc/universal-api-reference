# Submit Clustering Job with GraphHopper

Submits a clustering job in GraphHopper.

## Endpoint

- **Method:** `POST`
- **Path:** `/cluster/calculate`
- **Base URL:** `https://graphhopper.com/api/1`
- **Official documentation:** [Submit Clustering Job](https://docs.graphhopper.com/openapi/clustering/postclustercalculate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestBody` | body | `object` | yes | Asynchronous clustering request JSON body matching GraphHopper's ClusterRequest schema. |
