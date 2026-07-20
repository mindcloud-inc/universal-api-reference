# Add Comment with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Add Comment](https://docs.leantime.io/api/classes/Leantime/Domain/Comments/Services/Comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.module` | body | `string` | yes | The Leantime module name. |
| `entityId` | body | `number` | yes | The target entity id. |
| `params.values.text` | body | `string` | yes | Comment text. |
| `params.values.father` | body | `number` | yes | Parent comment id; use 0 for a new top-level comment. |
| `params.values.status` | body | `string` | no | Optional comment status. |
