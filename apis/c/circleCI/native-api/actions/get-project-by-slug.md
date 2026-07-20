# Get Project By Slug with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:project_slug`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Get Project By Slug](https://circleci.com/docs/api/v2/#tag/Project/operation/getProjectBySlug)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
