# Get Endpoint with Svix

Retrieves an endpoint from Svix.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/app/{app_id}/endpoint/{endpoint_id}`
- **Base URL:** `https://api.us.svix.com`
- **Official documentation:** [Get Endpoint](https://api.svix.com/docs#operation/v1.endpoint.get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `string` | yes | The application's ID or UID. |
| `endpoint_id` | path | `string` | yes | The endpoint's ID or UID. |
