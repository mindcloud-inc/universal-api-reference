# Update Environment Variable with Cloud 66

Updates an environment variable in your Cloud 66 account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/stacks/:stack_id/environments/:env_var_key`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Update Environment Variable](https://developers.cloud66.com/v3/endpoints/environment-variables/#update-environment-variable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | The stack UID |
| `env_var_key` | path | `string` | yes | The environment variable key or name |
| `value` | body | `string` | yes | The new environment variable value |
