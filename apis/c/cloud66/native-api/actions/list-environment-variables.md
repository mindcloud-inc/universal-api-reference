# List Environment Variables with Cloud 66

Retrieves environment variables from your Cloud 66 account.

## Endpoint

- **Method:** `GET`
- **Path:** `/stacks/:stack_id/environments`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [List Environment Variables](https://developers.cloud66.com/v3/endpoints/environment-variables/#list-environment-variables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | The stack UID |
