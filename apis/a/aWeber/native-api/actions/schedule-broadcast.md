# Schedule Broadcast with AWeber

Schedules a broadcast in AWeber.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/lists/:listId/broadcasts/:broadcastId/schedule`
- **Base URL:** `https://api.aweber.com/1.0`
- **Official documentation:** [Schedule Broadcast](https://api.aweber.com/#tag/Broadcasts/paths/~1accounts~1{accountId}~1lists~1{listId}~1broadcasts~1{broadcastId}~1schedule/post)

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
| `scheduled_for` | body | `string` | yes |
