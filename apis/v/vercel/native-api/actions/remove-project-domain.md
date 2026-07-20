# Remove Project Domain with Vercel

Removes a domain from a Vercel project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v9/projects/:idOrName/domains/:domain`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Remove Project Domain](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/remove-a-domain-from-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | The unique project identifier or the project name |
| `domain` | path | `string` | yes | The project domain name |
