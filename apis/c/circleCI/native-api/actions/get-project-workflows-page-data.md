# Get Project Workflows Page Data with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/insights/pages/:project_slug/summary`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Get Project Workflows Page Data](https://circleci.com/docs/api/v2/#tag/Insights/operation/getProjectWorkflowsPageData)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
