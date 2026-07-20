# Restart compute endpoint with Neon

Restarts compute endpoint in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/endpoints/:endpoint_id/restart`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Restart compute endpoint](https://api-docs.neon.tech/reference/restartprojectendpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `endpoint_id` | path | `string` | yes | Neon API parameter endpoint_id |
