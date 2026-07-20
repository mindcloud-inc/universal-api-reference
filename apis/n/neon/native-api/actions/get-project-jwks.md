# List JWKS URLs with Neon

Retrieves JWKS URLs for a project from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/jwks`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [List JWKS URLs](https://api-docs.neon.tech/reference/getprojectjwks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
