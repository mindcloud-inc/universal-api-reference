# Create Project Env Vars with Vercel

Creates project environment variables in Vercel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v10/projects/:idOrName/env`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Create Project Env Vars](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/create-one-or-more-environment-variables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | The unique project identifier or the project name |
| `key` | body | `string` | yes | The name of the environment variable |
| `value` | body | `string` | yes | The value of the environment variable |
| `type` | body | `string` | yes | The type of environment variable |
| `target[0]` | body | `string` | yes | The target environment of the environment variable |
