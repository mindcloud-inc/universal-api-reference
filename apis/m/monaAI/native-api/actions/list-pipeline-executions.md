# List Pipeline Executions with Mona AI

Retrieves pipeline executions from Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/pipeline/executions`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [List Pipeline Executions](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineId` | body | `string` | yes | Pipeline identifier whose executions should be listed. |
