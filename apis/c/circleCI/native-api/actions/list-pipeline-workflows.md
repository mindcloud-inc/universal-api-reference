# List Pipeline Workflows with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/pipeline/:pipeline_id/workflow`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [List Pipeline Workflows](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/listWorkflowsByPipelineId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page-token` | query | `string` | no | Pagination cursor returned by CircleCI. |
| `pipeline_id` | path | `string` | no | Opaque pipeline identifier. |
