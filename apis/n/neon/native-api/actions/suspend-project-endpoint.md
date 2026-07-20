# Suspend compute endpoint with Neon

Suspends compute endpoint in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/endpoints/:endpoint_id/suspend`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Suspend compute endpoint](https://api-docs.neon.tech/reference/suspendprojectendpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `endpoint_id` | path | `string` | yes | Neon API parameter endpoint_id |
