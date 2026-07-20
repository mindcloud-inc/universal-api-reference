# Update Stack Setting with Cloud 66

Updates a stack setting in your Cloud 66 account.

## Endpoint

- **Method:** `PUT`
- **Path:** `/stacks/:stack_id/settings/:id`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Update Stack Setting](https://developers.cloud66.com/v3/endpoints/stack-settings/#update-stack-setting)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | The stack UID |
| `id` | path | `string` | yes | The setting item ID |
| `value` | body | `string` | yes | The setting item new value |
