# Get Pipeline Definition with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/pipeline-definitions/:pipeline_definition_id`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Get Pipeline Definition](https://circleci.com/docs/api/v2/#tag/Pipeline-Definition/operation/getPipelineDefinition)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipeline_definition_id` | path | `string` | no | Opaque pipeline definition identifier. |
| `project_id` | path | `string` | no | Opaque project identifier. |
