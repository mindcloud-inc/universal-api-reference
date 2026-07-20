# List Project Domains with Vercel

Retrieves all project domains from Vercel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v9/projects/:idOrName/domains`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [List Project Domains](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/retrieve-project-domains-by-project-by-id-or-name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | The unique project identifier or the project name |
