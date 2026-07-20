# Retrieve compute endpoint details with Neon

Retrieves compute endpoint details from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/endpoints/:endpoint_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Retrieve compute endpoint details](https://api-docs.neon.tech/reference/getprojectendpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `endpoint_id` | path | `string` | yes | Neon API parameter endpoint_id |
