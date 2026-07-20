# Delete Pipeline with CATS

Deletes an existing pipeline from CATS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/pipelines/:id`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Delete Pipeline](https://docs.catsone.com/api/v3/#pipelines-delete-a-pipeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the pipeline to delete. |
| `create_activity` | query | `boolean` | no | Whether a corresponding activity should be created automatically. |
