# List Broadcasts with AWeber

Retrieves broadcasts from AWeber.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/lists/:listId/broadcasts`
- **Base URL:** `https://api.aweber.com/1.0`
- **Official documentation:** [List Broadcasts](https://api.aweber.com/#tag/Broadcasts/paths/~1accounts~1{accountId}~1lists~1{listId}~1broadcasts/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `listId` | path | `string` | yes |
| `status` | query | `string` | yes |
