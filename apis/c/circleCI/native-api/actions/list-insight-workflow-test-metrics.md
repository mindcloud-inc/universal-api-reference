# List Insight Workflow Test Metrics with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/insights/:project_slug/workflows/:workflow_name/test-metrics`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [List Insight Workflow Test Metrics](https://circleci.com/docs/api/v2/#tag/Insights/operation/getProjectWorkflowTestMetrics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
| `workflow_name` | path | `string` | no | Workflow name. |
