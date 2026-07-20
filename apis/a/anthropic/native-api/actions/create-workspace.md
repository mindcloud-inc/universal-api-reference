# Create Workspace with Anthropic

Creates a workspace in the Anthropic organization.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/organizations/workspaces`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Create Workspace](https://platform.claude.com/docs/en/api/admin/workspaces/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Display name for the new workspace. |
