# Add Project Domain with Vercel

Adds a domain to a Vercel project.

## Endpoint

- **Method:** `POST`
- **Path:** `/v10/projects/:idOrName/domains`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Add Project Domain](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/add-a-domain-to-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | The unique project identifier or the project name |
| `name` | body | `string` | yes | The domain name to add to the project |
