# Get Endpoint Details with EMnify

Retrieves details for an endpoint from EMnify.

## Endpoint

- **Method:** `GET`
- **Path:** `/endpoint/:endpoint_id`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [Get Endpoint Details](https://docs.emnify.com/developers/api/endpoint/endpoint-by-id-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `endpoint_id` | path | `number` | yes | Endpoint ID to retrieve. |
