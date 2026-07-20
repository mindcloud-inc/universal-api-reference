# Update compute endpoint with Neon

Updates a compute endpoint in Neon.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/endpoints/:endpoint_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update compute endpoint](https://api-docs.neon.tech/reference/updateprojectendpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `endpoint_id` | path | `string` | yes | Neon API parameter endpoint_id |
| `endpoint` | body | `object` | yes | Neon API parameter endpoint |
