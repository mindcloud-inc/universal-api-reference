# List Available Tables with Selection Status with SingleStore

Retrieves available source tables and their ingestion selection status from SingleStore.

## Endpoint

- **Method:** `GET`
- **Path:** `/list-db/{database}/{schema}`
- **Base URL:** `https://{flowEndpoint}:30081/ingest/api/ingest`
- **Official documentation:** [List Available Tables with Selection Status](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#list-available-tables-with-selection-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `database` | path | `string` | yes | Database name in the source system. |
| `schema` | path | `string` | yes | Schema name inside the selected database. |
