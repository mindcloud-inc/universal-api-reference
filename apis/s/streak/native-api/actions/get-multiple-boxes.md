# Get multiple boxes with Streak

Retrieves multiple boxes from a Streak pipeline.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/pipelines/:pipelineKey/boxes/batch/`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [Get multiple boxes](https://streak.readme.io/reference/get-multiple-boxes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineKey` | path | `list<string>` | yes | The key of the pipeline containing the boxes to retrieve. |
| `boxKeys[]` | body | `array<string>` | yes | The box keys to retrieve. |
