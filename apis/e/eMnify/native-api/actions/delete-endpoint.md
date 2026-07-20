# Delete Endpoint with EMnify

Deletes an endpoint and its child entities from EMnify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/endpoint/:endpoint_id`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [Delete Endpoint](https://docs.emnify.com/developers/api/endpoint/endpoint-by-id-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `endpoint_id` | path | `number` | yes | Endpoint ID to delete. |
