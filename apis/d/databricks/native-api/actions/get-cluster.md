# Get Cluster with Databricks

Retrieves a cluster from the Databricks workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `{host}/api/2.1/clusters/get`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Get Cluster](https://docs.databricks.com/api/workspace/clusters/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cluster_id` | query | `string` | yes | The cluster about which to retrieve information. |
