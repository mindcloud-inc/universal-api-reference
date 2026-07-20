# Verify Project Domain with Vercel

Verifies a project domain in Vercel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v9/projects/:idOrName/domains/:domain/verify`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Verify Project Domain](https://docs.vercel.com/docs/rest-api/reference/endpoints/projects/verify-project-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idOrName` | path | `string` | yes | The unique project identifier or the project name |
| `domain` | path | `string` | yes | The project domain name |
