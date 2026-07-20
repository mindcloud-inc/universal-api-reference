# Delete Project Environment Variable with CircleCI

## Endpoint

- **Method:** `DELETE`
- **Path:** `/project/:project_slug/envvar/:name`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Delete Project Environment Variable](https://circleci.com/docs/api/v2/#tag/Environment-Variable/operation/deleteEnvVar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | no | Environment variable name. |
| `project_slug` | path | `string` | no | Project slug in the form vcs/org/repo. |
