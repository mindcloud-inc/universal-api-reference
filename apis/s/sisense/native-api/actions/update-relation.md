# Update Relation with Sisense

Updates an existing relation in Sisense.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/datamodels/:datamodelId/relations/:relationId`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Update Relation](https://developer.sisense.com/guides/restApi/datamodels.v2.html#updating-relations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columns[].column` | body | `string` | no | The column oid for a related column. |
| `columns[].dataset` | body | `string` | no | The dataset oid for a related column. |
| `columns[].table` | body | `string` | no | The table oid for a related column. |
| `datamodelId` | path | `string` | no | The Datamodel oid. |
| `relationId` | path | `string` | no | The Relation oid. |
