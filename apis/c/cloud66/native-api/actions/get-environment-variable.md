# Get Environment Variable with Cloud 66

Retrieves an environment variable from your Cloud 66 account.

## Endpoint

- **Method:** `GET`
- **Path:** `/stacks/:stack_id/environments/:env_var_id`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Get Environment Variable](https://developers.cloud66.com/v3/endpoints/environment-variables/#get-environment-variable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | The stack UID |
| `env_var_id` | path | `number` | yes | The environment variable ID |
