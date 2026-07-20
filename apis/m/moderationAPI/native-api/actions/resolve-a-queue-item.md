# Resolve A Queue Item with Moderation API

Resolves a review queue item in Moderation API.

## Endpoint

- **Method:** `POST`
- **Path:** `/queue/:id/items/:itemId/resolve`
- **Base URL:** `https://api.moderationapi.com/v1`
- **Official documentation:** [Resolve A Queue Item](https://docs.moderationapi.com/api-reference/review-queues/resolve-a-queue-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The queue ID |
| `itemId` | path | `string` | yes | The item ID to resolve |
| `comment` | body | `string` | no | Optional comment |
