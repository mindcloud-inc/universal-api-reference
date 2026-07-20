# Update Pipeline Definition with CircleCI

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/pipeline-definitions/:pipeline_definition_id`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Update Pipeline Definition](https://circleci.com/docs/api/v2/#tag/Pipeline-Definition/operation/updatePipelineDefinition)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkout_source` | body | `string` | no | Repository checkout source configuration. |
| `config_source` | body | `string` | no | Pipeline configuration source. |
| `description` | body | `string` | no | Pipeline definition description. |
| `name` | body | `string` | no | Pipeline definition name. |
| `pipeline_definition_id` | path | `string` | no | Opaque pipeline definition identifier. |
| `project_id` | path | `string` | no | Opaque project identifier. |
