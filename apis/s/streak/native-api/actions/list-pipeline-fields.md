# List Pipeline Fields with Streak

Retrieves pipeline fields from Streak.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/pipelines/:pipelineKey/fields`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [List Pipeline Fields](https://streak.readme.io/reference/list-all-fields-in-a-pipeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineKey` | path | `string` | yes | The key of the pipeline. |
