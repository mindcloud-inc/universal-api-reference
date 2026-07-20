# List Lists with Hey Reach

Retrieves lead and company lists from Hey Reach.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/list/GetAll`
- **Base URL:** `https://api.heyreach.io`
- **Official documentation:** [List Lists](https://documenter.getpostman.com/view/23808049/2sA2xb5F75)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `offset` | body | `number` | no |
| `keyword` | body | `string` | no |
| `listType` | body | `string` | no |
| `campaignIds[]` | body | `array<number>` | no |
| `limit` | body | `number` | no |
