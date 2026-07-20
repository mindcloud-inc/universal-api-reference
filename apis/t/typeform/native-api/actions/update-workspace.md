# Update Workspace with Typeform

## Endpoint

- **Method:** `PATCH`
- **Path:** `/workspaces/:workspaceId`
- **Base URL:** `https://api.typeform.com`
- **Official documentation:** [Update Workspace](https://www.typeform.com/developers/create/reference/update-workspace/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `op` | body | `string` | no | Patch operation. |
| `path` | body | `string` | no | JSON pointer path for the patch. |
| `value` | body | `string` | no | Patch value. |
| `workspaceId` | path | `string` | yes | Typeform workspace identifier. |
