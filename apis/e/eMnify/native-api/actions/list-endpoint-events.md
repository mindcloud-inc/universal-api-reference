# List Endpoint Events with EMnify

Retrieves events for an endpoint from EMnify.

## Endpoint

- **Method:** `GET`
- **Path:** `/endpoint/:endpoint_id/event`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [List Endpoint Events](https://docs.emnify.com/developers/api/endpoint/endpoint-events-by-id)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `endpoint_id` | path | `number` | yes | Numeric ID of an endpoint. |
| `q` | query | `string` | no | Optional event filter in <filter>:<value> format. |
