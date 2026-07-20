# Delete Table Column with Sisense

Deletes a column from a Sisense table.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/datamodels/:datamodelId/datasets/:datasetId/tables/:tableId`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Delete Table Column](https://developer.sisense.com/guides/restApi/datamodels.v2.html#deleting-a-column)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columns[].id` | body | `string` | no | The identifier of a column to keep after deletion. |
| `columns[].name` | body | `string` | no | The name of a column to keep after deletion. |
| `columns[].oid` | body | `string` | no | The oid of a column to keep after deletion. |
| `columns[].type` | body | `string` | no | The Sisense column type integer for a remaining column. |
| `datamodelId` | path | `string` | no | The Datamodel oid. |
| `datasetId` | path | `string` | no | The Dataset oid. |
| `tableId` | path | `string` | no | The Table oid. |
