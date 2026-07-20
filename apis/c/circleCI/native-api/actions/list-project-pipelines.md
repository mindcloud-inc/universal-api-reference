# List Project Pipelines with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:project_slug/pipeline`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [List Project Pipelines](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/listPipelinesForProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page-token` | query | `string` | no | Pagination cursor returned by CircleCI. |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
