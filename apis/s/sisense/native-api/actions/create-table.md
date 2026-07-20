# Create Table with Sisense

Creates a table in a Sisense dataset.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/datamodels/:datamodelId/datasets/:datasetId/tables`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Create Table](https://developer.sisense.com/guides/restApi/datamodels.v2.html#creating-a-table)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `datamodelId` | path | `string` | yes |
| `datasetId` | path | `string` | yes |
| `id` | body | `string` | yes |
| `name` | body | `string` | yes |
| `type` | body | `string` | yes |
| `expression` | body | `string` | yes |
