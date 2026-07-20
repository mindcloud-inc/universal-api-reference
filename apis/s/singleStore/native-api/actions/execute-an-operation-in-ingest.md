# Execute an Operation in Ingest with SingleStore

Executes an ingest operation in SingleStore.

## Endpoint

- **Method:** `POST`
- **Path:** `/ops/extract/{operation}`
- **Base URL:** `https://{flowEndpoint}:30081/ingest/api/ingest`
- **Official documentation:** [Execute an Operation in Ingest](https://docs.singlestore.com/cloud/load-data/load-data-with-singlestore-flow-on-helios/flow-on-helios-api/flow-on-helios-ingest-api/#execute-an-operation-in-ingest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `operation` | path | `string` | yes | Ingest operation to execute. The docs show full, syncnew, syncstruct, and delta. |
