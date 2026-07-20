# Get Project Domain with Vercel

Retrieves a project domain from Vercel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v9/projects/:idOrName/domains/:domain`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Get Project Domain](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/get-a-project-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | The unique project identifier or the project name |
| `domain` | path | `string` | yes | The project domain name |
