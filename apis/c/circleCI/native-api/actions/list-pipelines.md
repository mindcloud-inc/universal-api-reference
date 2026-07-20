# List Pipelines with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/pipeline`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [List Pipelines](https://circleci.com/docs/api/v2/#tag/Pipeline/operation/listPipelinesForProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org-slug` | query | `string` | yes | Organization slug in the form vcs-slug/org-name. |
