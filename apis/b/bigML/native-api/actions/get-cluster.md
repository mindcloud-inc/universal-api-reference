# Get Cluster with BigML

Retrieves a cluster from BigML.

## Endpoint

- **Method:** `GET`
- **Path:** `/cluster/:clusterId`
- **Base URL:** `https://bigml.io`
- **Official documentation:** [Get Cluster](https://bigml.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clusterId` | path | `string` | yes | BigML cluster identifier suffix only (for example, 69cd1234abcd1234abcd1234). Do not include cluster/. |
