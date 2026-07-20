# Add Custom Column To Table with Sisense

Adds a custom column to a Sisense table.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/datamodels/:datamodelId/datasets/:datasetId/tables/:tableId`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Add Custom Column To Table](https://developer.sisense.com/guides/restApi/datamodels.v2.html#updating-or-removing-a-table-s-columns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columns[].expression` | body | `string` | no | The SQL expression for the custom column. |
| `columns[].id` | body | `string` | no | The new custom column identifier. |
| `columns[].isCustom` | body | `string` | no | Set to true for the custom column. |
| `columns[].name` | body | `string` | no | The new custom column display name. |
| `columns[].oid` | body | `string` | no | The oid of an existing column to keep in the table payload. |
| `columns[].type` | body | `string` | no | The Sisense column type integer. |
| `datamodelId` | path | `string` | no | The Datamodel oid. |
| `datasetId` | path | `string` | no | The Dataset oid. |
| `tableId` | path | `string` | no | The Table oid. |
