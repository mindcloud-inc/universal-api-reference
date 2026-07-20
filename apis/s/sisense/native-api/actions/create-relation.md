# Create Relation with Sisense

Creates a relation in a Sisense datamodel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/datamodels/:datamodelId/relations`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Create Relation](https://developer.sisense.com/guides/restApi/datamodels.v2.html#creating-a-relation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `datamodelId` | path | `string` | yes |
| `columns[0].dataset` | body | `string` | yes |
| `columns[0].table` | body | `string` | yes |
| `columns[0].column` | body | `string` | yes |
| `columns[1].dataset` | body | `string` | yes |
| `columns[1].table` | body | `string` | yes |
| `columns[1].column` | body | `string` | yes |
