# List Subscribers with AWeber

Retrieves subscribers from AWeber.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/lists/:listId/subscribers`
- **Base URL:** `https://api.aweber.com/1.0`
- **Official documentation:** [List Subscribers](https://api.aweber.com/#tag/Subscribers/paths/~1accounts~1{accountId}~1lists~1{listId}~1subscribers/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `listId` | path | `string` | yes |
| `sort_order` | query | `string` | no |
