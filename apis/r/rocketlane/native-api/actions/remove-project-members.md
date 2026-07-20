# Remove Project Members with Rocketlane

Removes members from a project in Rocketlane.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.0/projects/:projectId/remove-members`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Remove Project Members](https://developer.rocketlane.com/reference/remove-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The project's unique, system-generated identifier, which can be used to identify the project globally. |
| `members` | body | `list<object>` | yes | The team members from your organization working on the project. |
