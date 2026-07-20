# Add Member to Space with Superthread

## Endpoint

- **Method:** `POST`
- **Path:** `/:team_id/projects/:project_id/members`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Add Member to Space](https://superthread.com/docs/api-docs/spaces/add-member-to-a-space)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `project_id` | path | `string` | yes | Space ID to update membership for. |
| `members[]` | body | `array<object>` | yes | Members to add to the space. |
