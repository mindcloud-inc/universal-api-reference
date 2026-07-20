# Add Project Collaborators with ArcSite

Adds collaborators to an existing ArcSite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/add_collaborators`
- **Base URL:** `https://api.arcsite.com/v1`
- **Official documentation:** [Add Project Collaborators](https://dev.arcsite.com/#add-project-collaborators)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The ID of the project. |
| `collaborators[]` | body | `array<object>` | yes | Collaborators to add to the project. |
