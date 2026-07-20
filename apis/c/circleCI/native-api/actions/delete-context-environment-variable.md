# Delete Context Environment Variable with CircleCI

## Endpoint

- **Method:** `DELETE`
- **Path:** `/context/:context_id/environment-variable/:env_var_name`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Delete Context Environment Variable](https://circleci.com/docs/api/v2/#tag/Context/operation/deleteEnvironmentVariableFromContext)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `context_id` | path | `string` | no | The CircleCI context UUID. |
| `env_var_name` | path | `string` | no | The environment variable name. |
