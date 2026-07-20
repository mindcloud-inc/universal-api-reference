# Import Project Template with Rocketlane

Imports a project template into Rocketlane.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.0/projects/:projectId/import-template`
- **Base URL:** `https://api.rocketlane.com/api`
- **Official documentation:** [Import Project Template](https://developer.rocketlane.com/reference/import-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The project's unique, system-generated identifier, which can be used to identify the project globally. |
