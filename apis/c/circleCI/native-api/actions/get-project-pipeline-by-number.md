# Get Project Pipeline By Number with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:project_slug/pipeline/:pipeline_number`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Get Project Pipeline By Number](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/getPipelineByNumber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipeline_number` | path | `string` | no | Pipeline number within the project. |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
