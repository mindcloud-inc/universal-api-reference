# Cancel Scheduled Broadcast with AWeber

Cancels a scheduled broadcast in AWeber.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/lists/:listId/broadcasts/:broadcastId/cancel`
- **Base URL:** `https://api.aweber.com/1.0`
- **Official documentation:** [Cancel Scheduled Broadcast](https://api.aweber.com/#tag/Broadcasts/paths/~1accounts~1{accountId}~1lists~1{listId}~1broadcasts~1{broadcastId}~1cancel/post)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `broadcastId` | path | `string` | yes |
| `listId` | path | `string` | yes |
