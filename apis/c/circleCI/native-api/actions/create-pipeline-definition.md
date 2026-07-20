# Create Pipeline Definition with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/pipeline-definitions`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Create Pipeline Definition](https://circleci.com/docs/api/v2/#tag/Pipeline-Definition/operation/createPipelineDefinition)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkout_source` | body | `string` | no | Repository checkout source configuration. |
| `config_source` | body | `string` | no | Pipeline configuration source. |
| `description` | body | `string` | no | Pipeline definition description. |
| `name` | body | `string` | no | Pipeline definition name. |
| `project_id` | path | `string` | no | Opaque project identifier. |
