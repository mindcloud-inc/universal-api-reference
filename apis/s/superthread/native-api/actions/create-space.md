# Create Space with Superthread

## Endpoint

- **Method:** `POST`
- **Path:** `/:team_id/projects`
- **Base URL:** `https://api.superthread.com/v1`
- **Official documentation:** [Create Space](https://superthread.com/docs/api-docs/spaces/create-a-space)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | yes | Workspace ID for the Superthread workspace. |
| `title` | body | `string` | yes | Space title. |
