# Retrieve Endpoint Data Quota Details with EMnify

Retrieves endpoint data quota details from EMnify.

## Endpoint

- **Method:** `GET`
- **Path:** `/endpoint/:endpoint_id/quota/data`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [Retrieve Endpoint Data Quota Details](https://docs.emnify.com/developers/api/endpoint/endpoint-quota-data-by-endpoint-id-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `endpoint_id` | path | `number` | yes | Endpoint ID to inspect. |
