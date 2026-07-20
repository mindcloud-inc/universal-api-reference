# Create Workspace Member with Anthropic

Adds a member to an Anthropic workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/organizations/workspaces/{workspace_id}/members`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Create Workspace Member](https://platform.claude.com/docs/en/api/admin/workspaces/members/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | path | `string` | yes | Workspace ID where member will be added. |
| `user_id` | body | `string` | yes | User ID to add as member. |
| `workspace_role` | body | `string` | yes | Role to grant in workspace. |
