# Remove Project Collaborator with zipBoard

Removes a project collaborator from zipBoard.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/project/:id/collaborators`
- **Base URL:** `https://app.zipboard.co/api/v1`
- **Official documentation:** [Remove Project Collaborator](https://docs.zipboard.co/#tag/Collaborators/paths/~1api~1v1~1project~1{id}~1collaborators/delete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `id` | path | `string` | yes |
