# Delete Pipeline Definition with CircleCI

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/pipeline-definitions/:pipeline_definition_id`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Delete Pipeline Definition](https://circleci.com/docs/api/v2/#tag/Pipeline-Definition/operation/deletePipelineDefinition)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipeline_definition_id` | path | `string` | no | Opaque pipeline definition identifier. |
| `project_id` | path | `string` | no | Opaque project identifier. |
