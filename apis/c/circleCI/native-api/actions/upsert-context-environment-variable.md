# Upsert Context Environment Variable with CircleCI

## Endpoint

- **Method:** `PUT`
- **Path:** `/context/:context_id/environment-variable/:env_var_name`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Upsert Context Environment Variable](https://circleci.com/docs/api/v2/#tag/Context/operation/addEnvironmentVariableToContext)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `context_id` | path | `string` | no | The CircleCI context UUID. |
| `env_var_name` | path | `string` | no | The environment variable name. |
| `value` | body | `string` | yes | The environment variable value. |
