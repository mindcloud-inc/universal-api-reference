# Get Pipeline with Streak

Retrieves a pipeline from Streak.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/pipelines/:pipelineKey`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [Get Pipeline](https://streak.readme.io/reference/getting-a-specific-pipeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineKey` | path | `list<string>` | yes | The key of the pipeline to retrieve. |
