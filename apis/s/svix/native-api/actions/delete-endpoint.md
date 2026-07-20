# Delete Endpoint with Svix

Deletes an endpoint from Svix.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/app/{app_id}/endpoint/{endpoint_id}`
- **Base URL:** `https://api.us.svix.com`
- **Official documentation:** [Delete Endpoint](https://api.svix.com/docs#operation/v1.endpoint.delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `string` | yes | The application's ID or UID. |
| `endpoint_id` | path | `string` | yes | The endpoint's ID or UID. |
