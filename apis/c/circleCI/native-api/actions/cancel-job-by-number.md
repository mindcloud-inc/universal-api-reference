# Cancel Job By Number with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/project/:project_slug/job/:job_number/cancel`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Cancel Job By Number](https://circleci.com/docs/api/v2/#tag/Job/operation/cancelJobByJobNumber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_number` | path | `string` | no | Job number within the project. |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
