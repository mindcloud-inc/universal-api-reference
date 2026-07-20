# Archive Project with Rocketlane

Archives a project in Rocketlane.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.0/projects/:projectId/archive`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Archive Project](https://developer.rocketlane.com/reference/archiveProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The project's unique, system-generated identifier, which can be used to identify the project globally. |
