# Restart Cluster with Databricks

Restarts an existing cluster in the Databricks workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `{host}/api/2.1/clusters/restart`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Restart Cluster](https://docs.databricks.com/api/workspace/clusters/restart)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cluster_id` | body | `string` | yes | The cluster to be started. |
| `restart_user` | body | `string` | no | — |
