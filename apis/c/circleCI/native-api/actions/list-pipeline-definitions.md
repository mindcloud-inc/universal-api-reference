# List Pipeline Definitions with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/pipeline-definitions`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [List Pipeline Definitions](https://circleci.com/docs/api/v2/#tag/Pipeline-Definition/operation/listPipelineDefinitions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | no | Opaque project identifier. |
