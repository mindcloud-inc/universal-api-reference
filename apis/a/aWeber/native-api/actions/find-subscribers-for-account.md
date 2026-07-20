# Find Subscribers For Account with AWeber

Finds subscribers in an AWeber account.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId`
- **Base URL:** `https://api.aweber.com/1.0`
- **Official documentation:** [Find Subscribers For Account](https://api.aweber.com/#tag/Subscribers/paths/~1accounts~1{accountId}?ws.op=findSubscribers/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `email` | query | `string` | no |
| `name` | query | `string` | no |
| `status` | query | `string` | no |
| `tags` | query | `string` | no |
