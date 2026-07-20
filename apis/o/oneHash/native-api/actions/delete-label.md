# Delete Label with OneHash

Deletes an existing label from OneHash.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/accounts/:accountId/labels/:id`
- **Base URL:** `https://chat.onehash.ai`
- **Official documentation:** [Delete Label](https://developers.chatwoot.com/api-reference/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | no | OneHash Chat account id. |
| `id` | path | `string` | no | Label id. |
