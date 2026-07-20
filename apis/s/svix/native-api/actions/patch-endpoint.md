# Patch Endpoint with Svix

Updates an endpoint in Svix.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/app/{app_id}/endpoint/{endpoint_id}`
- **Base URL:** `https://api.us.svix.com`
- **Official documentation:** [Patch Endpoint](https://api.svix.com/docs#operation/v1.endpoint.patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `string` | yes | The application's ID or UID. |
| `endpoint_id` | path | `string` | yes | The endpoint's ID or UID. |
