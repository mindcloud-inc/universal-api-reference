# Delete Cluster with Databricks

Deletes an existing cluster from the Databricks workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `{host}/api/2.1/clusters/delete`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Delete Cluster](https://docs.databricks.com/api/workspace/clusters/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cluster_id` | body | `string` | yes | The cluster to be terminated. |
