# List Project Environment Variables with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:project_slug/envvar`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [List Project Environment Variables](https://circleci.com/docs/api/v2/#tag/Environment-Variable/operation/listEnvVars)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
