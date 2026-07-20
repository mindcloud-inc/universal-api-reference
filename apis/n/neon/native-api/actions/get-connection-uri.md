# Retrieve connection URI with Neon

Retrieves a connection URI from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/connection_uri`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Retrieve connection URI](https://api-docs.neon.tech/reference/getconnectionuri)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | query | `string` | no | Neon API parameter branch_id |
| `endpoint_id` | query | `string` | no | Neon API parameter endpoint_id |
| `database_name` | query | `string` | yes | Neon API parameter database_name |
| `role_name` | query | `string` | yes | Neon API parameter role_name |
| `pooled` | query | `boolean` | no | Neon API parameter pooled |
