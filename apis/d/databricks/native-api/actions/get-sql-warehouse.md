# Get SQL Warehouse with Databricks

Retrieves a SQL warehouse from the Databricks workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `{host}/api/2.0/sql/warehouses/:warehouseId`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Get SQL Warehouse](https://docs.databricks.com/api/workspace/warehouses/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Required. Id of the SQL warehouse. |
