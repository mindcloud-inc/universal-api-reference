# List Insight Branches with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/insights/:project_slug/branches`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [List Insight Branches](https://circleci.com/docs/api/v2/#tag/Insights/operation/getAllInsightsBranches)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
