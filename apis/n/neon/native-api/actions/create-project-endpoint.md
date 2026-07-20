# Create compute endpoint with Neon

Creates a compute endpoint in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/endpoints`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Create compute endpoint](https://api-docs.neon.tech/reference/createprojectendpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `endpoint` | body | `object` | yes | Neon API parameter endpoint |
