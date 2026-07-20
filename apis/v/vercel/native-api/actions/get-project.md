# Get Project with Vercel

Retrieves a project record from Vercel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v9/projects/:idOrName`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Get Project](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/find-a-project-by-id-or-name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | The unique project identifier or the project name |
