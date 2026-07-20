# Get Job Artifacts with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:project_slug/:job_number/artifacts`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Get Job Artifacts](https://circleci.com/docs/api/v2/#tag/Artifacts/operation/getJobArtifacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_number` | path | `string` | no | Job number within the project. |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
