# List Stack Actions with Cloud 66

Retrieves stack actions from your Cloud 66 account.

## Endpoint

- **Method:** `GET`
- **Path:** `/stacks/:id/actions`
- **Base URL:** `https://app.cloud66.com/api/3`
- **Official documentation:** [List Stack Actions](https://developers.cloud66.com/v3/endpoints/stacks/#stack-actions-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the stack. |
| `user_reference` | query | `string` | no | Filter actions by metadata value. |
