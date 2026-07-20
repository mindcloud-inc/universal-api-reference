# Select a Table for Ingestion with SingleStore

Updates whether a source table is selected for ingestion in SingleStore.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/config-tab/{database}/{schema}/{table}`
- **Base URL:** `https://{flowEndpoint}:30081/ingest/api/ingest`
- **Official documentation:** [Select a Table for Ingestion](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#select-a-table-for-ingestion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `database` | path | `string` | yes | Database name in the source system. |
| `schema` | path | `string` | yes | Schema name inside the selected database. |
| `table` | path | `string` | yes | Table name to update for ingestion. |
| `select` | body | `string` | yes | Whether the table should be selected for ingestion. |
