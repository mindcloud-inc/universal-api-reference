# Get Endpoint Usage And Cost Statistics with EMnify

Retrieves endpoint usage and cost statistics from EMnify.

## Endpoint

- **Method:** `GET`
- **Path:** `/endpoint/:endpoint_id/stats`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [Get Endpoint Usage And Cost Statistics](https://docs.emnify.com/developers/api/endpoint/endpoint-stats-by-id-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `endpoint_id` | path | `number` | yes | Endpoint ID to inspect. |
