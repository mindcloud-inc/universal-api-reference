# Start compute endpoint with Neon

Starts compute endpoint in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/endpoints/:endpoint_id/start`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Start compute endpoint](https://api-docs.neon.tech/reference/startprojectendpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `endpoint_id` | path | `string` | yes | Neon API parameter endpoint_id |
