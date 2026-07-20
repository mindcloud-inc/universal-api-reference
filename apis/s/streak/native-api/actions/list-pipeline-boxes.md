# List Pipeline Boxes with Streak

Retrieves boxes from a Streak pipeline.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/pipelines/:pipelineKey/boxes`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [List Pipeline Boxes](https://streak.readme.io/reference/list-all-boxes-in-pipeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineKey` | path | `list<string>` | yes | The key of the pipeline whose boxes to list. |
| `sortBy` | query | `list<string>` | no | What order to sort the boxes by. Valid values are creationTimestamp and lastUpdatedTimestamp. Accepted values: `creationTimestamp`, `lastUpdatedTimestamp`. |
| `stageKey` | query | `string` | no | Stage to search. Returns boxes in only the specified stage. |
