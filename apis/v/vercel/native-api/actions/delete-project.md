# Delete Project with Vercel

Deletes an existing project from Vercel.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v9/projects/:idOrName`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Delete Project](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/delete-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | The unique project identifier or the project name |
