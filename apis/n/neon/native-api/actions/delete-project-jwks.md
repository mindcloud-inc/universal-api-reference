# Delete JWKS URL with Neon

Deletes a JWKS URL from a project in Neon.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/jwks/:jwks_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Delete JWKS URL](https://api-docs.neon.tech/reference/deleteprojectjwks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `jwks_id` | path | `string` | yes | Neon API parameter jwks_id |
