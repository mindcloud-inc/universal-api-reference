# Find Subscribers For List with AWeber

Finds subscribers in an AWeber list.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/lists/:listId/subscribers`
- **Base URL:** `https://api.aweber.com/1.0`
- **Official documentation:** [Find Subscribers For List](https://api.aweber.com/#tag/Subscribers/paths/~1accounts~1{accountId}~1lists~1{listId}~1subscribers?ws.op=find/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `email` | query | `string` | no |
| `listId` | path | `string` | yes |
| `name` | query | `string` | no |
| `status` | query | `string` | no |
| `tags` | query | `string` | no |
