# Delete Project Env Var with Vercel

Deletes an existing project environment variable from Vercel.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v9/projects/:idOrName/env/:id`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Delete Project Env Var](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/remove-an-environment-variable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | The unique project identifier or the project name |
| `id` | path | `string` | yes | The unique environment variable identifier |
