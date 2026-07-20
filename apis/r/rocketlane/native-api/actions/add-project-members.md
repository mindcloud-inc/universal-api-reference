# Add Project Members with Rocketlane

Adds members to a project in Rocketlane.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.0/projects/:projectId/add-members`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Add Project Members](https://developer.rocketlane.com/reference/add-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The project's unique, system-generated identifier, which can be used to identify the project globally. |
| `members` | body | `list<object>` | no | The project team members. |
| `customers` | body | `list<object>` | no | The project customers. |
