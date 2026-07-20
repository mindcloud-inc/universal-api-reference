# Delete Relation with Sisense

Deletes an existing relation from Sisense.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/datamodels/:datamodelId/relations/:relationId`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Delete Relation](https://developer.sisense.com/guides/restApi/datamodels.v2.html#deleting-relations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datamodelId` | path | `string` | no | The Datamodel oid. |
| `relationId` | path | `string` | no | The Relation oid. |
