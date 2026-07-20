# Update Project Env Var with Vercel

Updates an existing project environment variable in Vercel.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v9/projects/:idOrName/env/:id`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Update Project Env Var](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/edit-an-environment-variable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | The unique project identifier or the project name |
| `id` | path | `string` | yes | The unique environment variable identifier |
| `key` | body | `string` | no | The name of the environment variable |
| `value` | body | `string` | no | The value of the environment variable |
| `type` | body | `string` | no | The type of environment variable |
| `target[0]` | body | `string` | no | The target environment of the environment variable |
