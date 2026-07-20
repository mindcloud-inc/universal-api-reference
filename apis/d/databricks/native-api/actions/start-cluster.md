# Start Cluster with Databricks

Starts an existing cluster in the Databricks workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `{host}/api/2.1/clusters/start`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Start Cluster](https://docs.databricks.com/api/workspace/clusters/start)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cluster_id` | body | `string` | yes | The cluster to be started. |
