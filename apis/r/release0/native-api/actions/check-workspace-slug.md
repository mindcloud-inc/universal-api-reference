# Check Workspace Slug with Release0

Checks whether a workspace slug is available in Release0.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/workspaces/:slug/exists`
- **Base URL:** `https://release0.com/api`
- **Official documentation:** [Check Workspace Slug](https://docs.release0.com/workspace/general)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | The workspace slug to check. |
