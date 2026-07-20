# Create Project Environment Variable with CircleCI

## Endpoint

- **Method:** `POST`
- **Path:** `/project/:project_slug/envvar`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Create Project Environment Variable](https://circleci.com/docs/api/v2/#tag/Environment-Variable/operation/createEnvVar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Environment variable name. |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
| `value` | body | `string` | no | Environment variable value. |
