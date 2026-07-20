# Get Job Timeseries with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/insights/time-series/:project_slug/workflows/:workflow_name/jobs`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Get Job Timeseries](https://circleci.com/docs/api/v2/#tag/Insights/operation/getJobTimeseries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
| `workflow_name` | path | `string` | no | Workflow name. |
