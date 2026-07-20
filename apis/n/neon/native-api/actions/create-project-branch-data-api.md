# Create Neon Data API with Neon

Creates Neon Data API configuration in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/branches/:branch_id/data-api/:database_name`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Create Neon Data API](https://api-docs.neon.tech/reference/createprojectbranchdataapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `database_name` | path | `string` | yes | Neon API parameter database_name |
| `auth_provider` | body | `list` | no | Neon API parameter auth_provider Accepted values: `0`, `1`. |
| `jwks_url` | body | `string` | no | Neon API parameter jwks_url |
| `provider_name` | body | `string` | no | Neon API parameter provider_name |
| `jwt_audience` | body | `string` | no | Neon API parameter jwt_audience |
| `add_default_grants` | body | `boolean` | no | Neon API parameter add_default_grants |
| `skip_auth_schema` | body | `boolean` | no | Neon API parameter skip_auth_schema |
| `settings` | body | `object` | no | Neon API parameter settings |
