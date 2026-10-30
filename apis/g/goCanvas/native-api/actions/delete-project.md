# Delete Project with GoCanvas

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:projectId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Delete Project](https://api.gocanvas.com/api/v3/docs#delete-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | — |
| `hard_delete` | query | `boolean` | no | Permanently deletes the project when true. Omit for soft delete. |
