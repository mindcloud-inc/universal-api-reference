# List Sandboxes V2 with E2B

Retrieves a list of sandboxes from E2B.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/sandboxes`
- **Base URL:** `https://api.e2b.app`
- **Official documentation:** [List Sandboxes V2](https://e2b.dev/docs/api-reference/sandboxes/list-sandboxes-v2)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metadata` | query | `string` | no | Optional URL-encoded metadata query used to filter sandboxes. |
| `state` | query | `string` | no | Filter sandboxes by one or more states. |
