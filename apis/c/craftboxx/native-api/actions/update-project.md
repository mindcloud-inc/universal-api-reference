# Update Project with Craftboxx

Updates a project in Craftboxx.

## Endpoint

- **Method:** `PUT`
- **Path:** `projects/:projectId`
- **Base URL:** `https://api.craftboxx.de`
- **Official documentation:** [Update Project](https://api.craftboxx.de/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The Craftboxx project ID. |
| `title` | body | `string` | no | The project title. |
