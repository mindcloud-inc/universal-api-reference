# List Conversations with Hey Reach

Retrieves LinkedIn conversations from Hey Reach.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/inbox/GetConversationsV2`
- **Base URL:** `https://api.heyreach.io`
- **Official documentation:** [List Conversations](https://documenter.getpostman.com/view/23808049/2sA2xb5F75)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters` | body | `object` | no |
| `offset` | body | `number` | no |
| `limit` | body | `number` | no |
