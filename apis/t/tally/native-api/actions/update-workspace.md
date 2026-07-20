# Update Workspace with Tally

## Endpoint

- **Method:** `PATCH`
- **Path:** `workspaces/:workspaceId`
- **Base URL:** `https://api.tally.so`
- **Official documentation:** [Update Workspace](https://developers.tally.so/api-reference/endpoint/workspaces/patch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `name` | body | `string` | yes |
