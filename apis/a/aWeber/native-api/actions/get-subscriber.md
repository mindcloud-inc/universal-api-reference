# Get Subscriber with AWeber

Retrieves a subscriber from AWeber.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/lists/:listId/subscribers/:subscriberId`
- **Base URL:** `https://api.aweber.com/1.0`
- **Official documentation:** [Get Subscriber](https://api.aweber.com/#tag/Subscribers/paths/~1accounts~1{accountId}~1lists~1{listId}~1subscribers~1{subscriberId}/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `listId` | path | `string` | yes |
| `subscriberId` | path | `string` | yes |
