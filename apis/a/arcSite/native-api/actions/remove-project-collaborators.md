# Remove Project Collaborators with ArcSite

Removes collaborators from an existing ArcSite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/remove_collaborators`
- **Base URL:** `https://api.arcsite.com/v1`
- **Official documentation:** [Remove Project Collaborators](https://dev.arcsite.com/#remove-project-collaborators)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The ID of the project. |
| `emails[]` | body | `array<string>` | yes | Collaborator emails to remove. |
