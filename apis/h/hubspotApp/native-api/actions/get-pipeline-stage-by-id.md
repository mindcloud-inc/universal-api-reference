# Get Pipeline Stage by ID with HubSpot

Retrieves a pipeline stage from HubSpot by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/pipelines/:objectType/:pipelineId/stages/:stageId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Get Pipeline Stage by ID](https://developers.hubspot.com/docs/api-reference/crm-pipelines-v3/pipeline-stages/get-crm-v3-pipelines-objectType-pipelineId-stages-stageId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectType` | path | `string` | yes | The object type whose pipeline stage to retrieve, such as deals or tickets. |
| `pipelineId` | path | `string` | yes | The ID of the pipeline that contains the stage. |
| `stageId` | path | `string` | yes | The ID of the pipeline stage to retrieve. |
