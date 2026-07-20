# List Pipeline Stages with Streak

Retrieves pipeline stages from Streak.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/pipelines/:pipelineKey/stages`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [List Pipeline Stages](https://streak.readme.io/reference/list-all-stages-in-pipeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineKey` | path | `string` | yes | Pipeline key for the pipeline whose stages you want to list. |
