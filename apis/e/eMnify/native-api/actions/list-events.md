# List Events with EMnify

Retrieves a list of events from EMnify.

## Endpoint

- **Method:** `GET`
- **Path:** `/event`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [List Events](https://docs.emnify.com/developers/api/events/get-events)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `q` | query | `string` | no | Optional event filter in <filter>:<value> format. |
