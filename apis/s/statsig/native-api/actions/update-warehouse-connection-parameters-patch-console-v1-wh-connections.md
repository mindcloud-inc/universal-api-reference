# Update Warehouse Connection Parameters with Statsig

Updates warehouse connection parameters in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/wh_connections`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update Warehouse Connection Parameters](https://docs.statsig.com/api-reference/warehouse-connections/update-warehouse-connection-parameters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databricks` | body | `object` | no | Request body field. |
| `snowflake` | body | `object` | no | Request body field. |
| `bigquery` | body | `object` | no | Request body field. |
| `redshift` | body | `object` | no | Request body field. |
| `athena` | body | `object` | no | Request body field. |
