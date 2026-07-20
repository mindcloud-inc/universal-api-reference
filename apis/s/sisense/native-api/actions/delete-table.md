# Delete Table with Sisense

Deletes an existing table from Sisense.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/datamodels/:datamodelId/datasets/:datasetId/tables/:tableId`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Delete Table](https://developer.sisense.com/guides/restApi/datamodels.v2.html#deleting-a-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datamodelId` | path | `string` | no | The Datamodel oid. |
| `datasetId` | path | `string` | no | The Dataset oid. |
| `tableId` | path | `string` | no | The Table oid. |
