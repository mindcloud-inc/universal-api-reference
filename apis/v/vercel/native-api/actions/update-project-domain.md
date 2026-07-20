# Update Project Domain with Vercel

Updates an existing project domain in Vercel.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v9/projects/:idOrName/domains/:domain`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Update Project Domain](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/update-a-project-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | The unique project identifier or the project name |
| `domain` | path | `string` | yes | The project domain name |
| `redirect` | body | `string` | no | The redirect target for the project domain |
