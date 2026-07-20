# Update Table with Sisense

Updates an existing table in Sisense.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/datamodels/:datamodelId/datasets/:datasetId/tables/:tableId`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Update Table](https://developer.sisense.com/guides/restApi/datamodels.v2.html#updating-a-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datamodelId` | path | `string` | no | The Datamodel oid. |
| `datasetId` | path | `string` | no | The Dataset oid. |
| `description` | body | `string` | no | An optional table description. |
| `name` | body | `string` | no | A new table name. |
| `tableId` | path | `string` | no | The Table oid. |
