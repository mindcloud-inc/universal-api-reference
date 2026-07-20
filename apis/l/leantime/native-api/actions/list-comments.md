# List Comments with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [List Comments](https://docs.leantime.io/api/classes/Leantime/Domain/Comments/Services/Comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.module` | body | `string` | yes | The Leantime module name. |
| `entityId` | body | `number` | yes | The target entity id. |
| `params.commentOrder` | body | `number` | no | 0 for oldest-first or 1 for newest-first. |
