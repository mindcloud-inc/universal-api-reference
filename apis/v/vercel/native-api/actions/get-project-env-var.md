# Get Project Env Var with Vercel

Retrieves a project environment variable from Vercel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:idOrName/env/:id`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Get Project Env Var](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/retrieve-the-decrypted-value-of-an-environment-variable-of-a-project-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | The unique project identifier or the project name |
| `id` | path | `string` | yes | The unique environment variable identifier |
