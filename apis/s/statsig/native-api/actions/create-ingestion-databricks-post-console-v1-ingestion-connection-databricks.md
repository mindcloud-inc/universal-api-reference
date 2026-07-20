# Create Ingestion Databricks with Statsig

Creates a Databricks ingestion in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/ingestion/connection/databricks`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Ingestion Databricks](https://docs.statsig.com/api-reference/ingestions/create-ingestion-databricks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | body | `string` | yes | Request body field. |
| `host` | body | `string` | yes | Request body field. |
| `path` | body | `string` | yes | Request body field. |
| `deltaSharingCredentials` | body | `string` | no | Request body field. |
| `verified` | body | `boolean` | no | Request body field. |
