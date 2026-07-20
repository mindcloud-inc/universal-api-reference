# List Endpoint SMS Messages with EMnify

Retrieves SMS messages for an endpoint from EMnify.

## Endpoint

- **Method:** `GET`
- **Path:** `/endpoint/:endpoint_id/sms`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [List Endpoint SMS Messages](https://docs.emnify.com/developers/api/endpoint/endpoint-sms-by-id-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `endpoint_id` | path | `number` | yes | Endpoint ID whose SMS messages should be listed. |
