# List Context Environment Variables with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/context/:context_id/environment-variable`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [List Context Environment Variables](https://circleci.com/docs/api/v2/#tag/Context/operation/listEnvironmentVariablesFromContext)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `context_id` | path | `string` | no | The CircleCI context UUID. |
