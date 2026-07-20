# Hide Or Show Table Column with Sisense

Updates a Sisense table column visibility.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/datamodels/:datamodelId/datasets/:datasetId/tables/:tableId`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Hide Or Show Table Column](https://developer.sisense.com/guides/restApi/datamodels.v2.html#updating-or-removing-a-table-s-columns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columns[].hidden` | body | `string` | no | Whether the column should be hidden. |
| `columns[].id` | body | `string` | no | The column identifier. |
| `columns[].name` | body | `string` | no | The column name. |
| `columns[].oid` | body | `string` | no | The oid of the existing column to update. |
| `columns[].type` | body | `string` | no | The Sisense column type integer. |
| `datamodelId` | path | `string` | no | The Datamodel oid. |
| `datasetId` | path | `string` | no | The Dataset oid. |
| `tableId` | path | `string` | no | The Table oid. |
