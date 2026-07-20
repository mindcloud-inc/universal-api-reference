# Get Pipeline by ID with HubSpot

Retrieves a pipeline from HubSpot by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/pipelines/:objectType/:pipelineId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Get Pipeline by ID](https://developers.hubspot.com/docs/api-reference/crm-pipelines-v3/pipelines/get-crm-v3-pipelines-objectType-pipelineId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectType` | path | `string` | yes | The object type whose pipeline to retrieve, such as deals or tickets. |
| `pipelineId` | path | `string` | yes | The ID of the pipeline to retrieve. |
