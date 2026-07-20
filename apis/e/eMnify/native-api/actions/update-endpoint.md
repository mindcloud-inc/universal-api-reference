# Update Endpoint with EMnify

Updates an existing endpoint in EMnify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/endpoint/:endpoint_id`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [Update Endpoint](https://docs.emnify.com/developers/api/endpoint/endpoint-by-id-patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `endpoint_id` | path | `number` | yes | Endpoint ID to update. |
| `name` | body | `string` | no | Updated endpoint name. |
| `status.id` | body | `number` | no | Updated endpoint status ID. |
