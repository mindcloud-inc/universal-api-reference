# Delete Project with CircleCI

## Endpoint

- **Method:** `DELETE`
- **Path:** `/project/:project_slug`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Delete Project](https://circleci.com/docs/api/v2/#tag/Project/operation/deleteProjectBySlug)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
