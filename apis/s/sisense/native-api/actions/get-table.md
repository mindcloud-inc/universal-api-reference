# Get Table with Sisense

Retrieves a table from a Sisense dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/datamodels/:datamodelId/datasets/:datasetId/tables/:tableId`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Get Table](https://developer.sisense.com/guides/restApi/datamodels.v2.html#endpoints)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `datamodelId` | path | `string` | yes |
| `datasetId` | path | `string` | yes |
| `tableId` | path | `string` | yes |
