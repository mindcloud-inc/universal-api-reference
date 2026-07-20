# Get Stack Action with Cloud 66

Retrieves a stack action from your Cloud 66 account.

## Endpoint

- **Method:** `GET`
- **Path:** `/stacks/:stack_id/actions/:id`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [Get Stack Action](https://developers.cloud66.com/v3/endpoints/stacks/#get-stack-action)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stack_id` | path | `string` | yes | Unique identifier of the stack. |
| `id` | path | `number` | yes | Identifier of the asynchronous action. |
