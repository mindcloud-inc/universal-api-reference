# List SQL Warehouses with Databricks

Retrieves SQL warehouses from the Databricks workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `{host}/api/2.0/sql/warehouses`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [List SQL Warehouses](https://docs.databricks.com/api/workspace/warehouses/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `run_as_user_id` | query | `number` | no | Deprecated: this field is ignored by the server. Service Principal which will be used to fetch the list of endpoints. If not specified, SQL Gateway will use the user from the session header. |
| `page_size` | query | `number` | no | The max number of warehouses to return. |
| `page_token` | query | `string` | no | A page token, received from a previous `ListWarehouses` call. Provide this to retrieve the subsequent page; otherwise the first will be retrieved.  When paginating, all other parameters provided to `ListWarehouses` must match the call that provided the page token. |
