# Create Project with Convex

Creates a new project in Convex.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/:team_id/create_project`
- **Base URL:** `https://api.convex.dev/v1`
- **Official documentation:** [Create Project](https://docs.convex.dev/management-api/create-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `number` | yes | The Convex team ID. |
| `projectName` | body | `string` | yes | The name of the project to create. |
