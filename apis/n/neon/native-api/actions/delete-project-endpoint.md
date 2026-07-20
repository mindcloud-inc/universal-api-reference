# Delete compute endpoint with Neon

Deletes a compute endpoint from Neon.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/endpoints/:endpoint_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Delete compute endpoint](https://api-docs.neon.tech/reference/deleteprojectendpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `endpoint_id` | path | `string` | yes | Neon API parameter endpoint_id |
