# Find Lists with AWeber

Finds lists in AWeber.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/lists`
- **Base URL:** `https://api.aweber.com/1.0`
- **Official documentation:** [Find Lists](https://api.aweber.com/#tag/Lists/paths/~1accounts~1{accountId}~1lists?ws.op=find/get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `string` | yes |
| `name` | query | `string` | no |
