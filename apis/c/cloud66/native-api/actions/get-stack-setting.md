# Get Stack Setting with Cloud 66

Retrieves a stack setting from your Cloud 66 account.

## Endpoint

- **Method:** `GET`
- **Path:** `/stacks/:stack_id/settings/:id`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Get Stack Setting](https://developers.cloud66.com/v3/endpoints/stack-settings/#get-stack-setting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | The stack UID |
| `id` | path | `string` | yes | The setting item ID |
