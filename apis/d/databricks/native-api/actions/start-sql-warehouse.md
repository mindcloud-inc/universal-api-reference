# Start SQL Warehouse with Databricks

Starts a SQL warehouse in the Databricks workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `{host}/api/2.0/sql/warehouses/:warehouseId/start`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Start SQL Warehouse](https://docs.databricks.com/api/workspace/warehouses/start)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Required. Id of the SQL warehouse. |
