# Get Broadcast with AWeber

Retrieves a broadcast from AWeber.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/lists/:listId/broadcasts/:broadcastId`
- **Base URL:** `https://api.aweber.com/1.0`
- **Official documentation:** [Get Broadcast](https://api.aweber.com/#tag/Broadcasts/paths/~1accounts~1{accountId}~1lists~1{listId}~1broadcasts~1{broadcastId}/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `broadcastId` | path | `string` | yes |
| `listId` | path | `string` | yes |
