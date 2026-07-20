# Assign Project Members with Trackabi

Assigns members to a project in Trackabi.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/projects/:projectId/assign-members`
- **Base URL:** `https://api.trackabi.com`
- **Official documentation:** [Assign Project Members](https://trackabi.com/help/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | The unique ID of the project. |
| `[]` | body | `array<object>` | yes | List of member assignment objects. |
| `[].member_id` | body | `number` | yes | Member ID. |
| `[].role_id` | body | `number` | no | Role ID. |
