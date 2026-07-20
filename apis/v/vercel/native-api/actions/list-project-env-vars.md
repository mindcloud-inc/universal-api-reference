# List Project Env Vars with Vercel

Retrieves project environment variables from Vercel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v10/projects/:idOrName/env`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [List Project Env Vars](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/retrieve-the-environment-variables-of-a-project-by-id-or-name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | The unique project identifier or the project name |
