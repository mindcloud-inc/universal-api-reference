# Update Pipeline with CATS

Updates an existing pipeline in CATS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/pipelines/:id`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Update Pipeline](https://docs.catsone.com/api/v3/#pipelines-update-a-pipeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the pipeline to update. |
| `rating` | body | `number` | yes | The candidate rating for the job. |
