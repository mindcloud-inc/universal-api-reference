# Update Label with OneHash

Updates an existing label in OneHash.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/accounts/:accountId/labels/:id`
- **Base URL:** `https://chat.onehash.ai`
- **Official documentation:** [Update Label](https://developers.chatwoot.com/api-reference/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | no | OneHash Chat account id. |
| `color` | body | `string` | no | Hex color. |
| `description` | body | `string` | no | Label description. |
| `id` | path | `string` | no | Label id. |
| `title` | body | `string` | no | Label title. |
