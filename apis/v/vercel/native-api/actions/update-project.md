# Update Project with Vercel

Updates an existing project in Vercel.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v9/projects/:idOrName`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Update Project](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/update-an-existing-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | The unique project identifier or the project name |
| `name` | body | `string` | no | The updated name for the project |
