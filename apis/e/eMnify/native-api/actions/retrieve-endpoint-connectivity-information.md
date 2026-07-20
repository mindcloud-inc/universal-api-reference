# Retrieve Endpoint Connectivity Information with EMnify

Retrieves connectivity information for an endpoint from EMnify.

## Endpoint

- **Method:** `GET`
- **Path:** `/endpoint/:endpoint_id/connectivity_info`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [Retrieve Endpoint Connectivity Information](https://docs.emnify.com/developers/api/endpoint/get-connectivity-info-by-endpoint-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `endpoint_id` | path | `number` | yes | Endpoint ID to inspect. |
| `subscriber` | query | `boolean` | no | Whether to request subscriber information in the connectivity lookup. |
