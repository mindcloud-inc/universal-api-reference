# Get Project Job Details with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:project_slug/job/:job_number`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Get Project Job Details](https://circleci.com/docs/api/v2/#tag/Job/operation/getJobDetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_number` | path | `string` | no | Job number within the project. |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
