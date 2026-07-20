# List Project Goals with Openlayer

Retrieves goals for a project in Openlayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/goals`
- **Base URL:** `https://api.openlayer.com/v1`
- **Official documentation:** [List Project Goals](https://api.openlayer.com/v1/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The Openlayer project ID. |
| `workspaceId` | query | `string` | yes | Workspace context required by Openlayer for project goal listing. |
