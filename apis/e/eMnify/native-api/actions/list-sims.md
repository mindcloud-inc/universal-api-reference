# List SIMs with EMnify

Retrieves a list of SIMs from EMnify.

## Endpoint

- **Method:** `GET`
- **Path:** `/sim`
- **Base URL:** `https://cdn.emnify.net/api/v1`
- **Official documentation:** [List SIMs](https://docs.emnify.com/developers/api/sim/sim-per-page-sort-by-q-and-page-get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth_token` | body | `string` | yes | Auth token from Retrieve Authentication Token. |
| `q` | query | `string` | no | Filter SIMs by search query. |
