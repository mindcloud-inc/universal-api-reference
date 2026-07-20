# Delete Dataset with Sisense

Deletes an existing dataset from Sisense.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/datamodels/:datamodelId/datasets/:datasetId`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Delete Dataset](https://developer.sisense.com/guides/restApi/datamodels.v2.html#deleting-a-dataset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datamodelId` | path | `string` | no | The Datamodel oid. |
| `datasetId` | path | `string` | no | The Dataset oid. |
