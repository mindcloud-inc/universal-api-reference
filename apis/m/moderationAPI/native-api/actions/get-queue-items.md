# Get Queue Items with Moderation API

Retrieves review queue items from Moderation API.

## Endpoint

- **Method:** `GET`
- **Path:** `/queue/:id/items`
- **Base URL:** `https://api.moderationapi.com/v1`
- **Official documentation:** [Get Queue Items](https://docs.moderationapi.com/api-reference/review-queues/get-queue-items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The queue ID |
| `pageSize` | query | `number` | no | Number of items per page |
| `pageNumber` | query | `number` | no | Page number to fetch |
| `sortField` | query | `string` | no | — |
| `sortDirection` | query | `string` | no | Sort direction |
| `conversationIds` | query | `string` | no | — |
| `labels` | query | `string` | no | — |
| `afterDate` | query | `string` | no | — |
| `beforeDate` | query | `string` | no | — |
| `includeResolved` | query | `string` | no | — |
| `authorId` | query | `string` | no | — |
| `filteredActionIds` | query | `string` | no | — |
