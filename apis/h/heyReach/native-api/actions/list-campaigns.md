# List Campaigns with Hey Reach

Retrieves campaigns from Hey Reach.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/campaign/GetAll`
- **Base URL:** `https://api.heyreach.io`
- **Official documentation:** [List Campaigns](https://documenter.getpostman.com/view/23808049/2sA2xb5F75)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `offset` | body | `number` | no |
| `keyword` | body | `string` | no |
| `statuses[]` | body | `array<string>` | no |
| `accountIds[]` | body | `array<number>` | no |
| `limit` | body | `number` | no |
