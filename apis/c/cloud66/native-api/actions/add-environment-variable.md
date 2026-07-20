# Add Environment Variable with Cloud 66

Creates an environment variable in your Cloud 66 account.

## Endpoint

- **Method:** `POST`
- **Path:** `/stacks/:stack_id/environments`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Add Environment Variable](https://developers.cloud66.com/v3/endpoints/environment-variables/#add-environment-variable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | The stack UID |
| `key` | body | `string` | yes | The environment variable key or name |
| `value` | body | `string` | yes | The environment variable value |
