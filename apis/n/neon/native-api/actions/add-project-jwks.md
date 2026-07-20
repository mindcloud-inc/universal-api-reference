# Add JWKS URL with Neon

Adds a JWKS URL to a project in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/jwks`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Add JWKS URL](https://api-docs.neon.tech/reference/addprojectjwks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `jwks_url` | body | `string` | yes | Neon API parameter jwks_url |
| `provider_name` | body | `string` | yes | Neon API parameter provider_name |
| `branch_id` | body | `string` | no | Neon API parameter branch_id |
| `jwt_audience` | body | `string` | no | Neon API parameter jwt_audience |
| `role_names[]` | body | `array<string>` | no | Neon API parameter role_names |
| `skip_role_creation` | body | `boolean` | no | Neon API parameter skip_role_creation |
