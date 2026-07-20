# List Connections with WorkOS

Retrieves connections from your WorkOS environment.

## Endpoint

- **Method:** `GET`
- **Path:** `/connections`
- **Base URL:** `https://api.workos.com`
- **Official documentation:** [List Connections](https://workos.com/docs/reference)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `string` | no | An object ID that defines your place in the list. When the ID is not present, you are at the end of the list. |
| `after` | query | `string` | no | An object ID that defines your place in the list. When the ID is not present, you are at the end of the list. |
| `limit` | query | `number` | no | Upper limit on the number of objects to return, between `1` and `100`. |
| `order` | query | `string` | no | Order the results by the creation time. |
| `organization_id` | query | `string` | no | Filter Connections by their associated organization. |
| `before` | query | `string` | no | An object ID that defines your place in the list. When the ID is not present, you are at the end of the list. |
| `after` | query | `string` | no | An object ID that defines your place in the list. When the ID is not present, you are at the end of the list. |
| `limit` | query | `number` | no | Upper limit on the number of objects to return, between `1` and `100`. |
| `order` | query | `string` | no | Order the results by the creation time. |
| `organization_id` | query | `string` | no | Filter Connections by their associated organization. |
