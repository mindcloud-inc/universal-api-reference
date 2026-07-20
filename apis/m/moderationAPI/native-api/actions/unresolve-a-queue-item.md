# Unresolve A Queue Item with Moderation API

Unresolves a review queue item in Moderation API.

## Endpoint

- **Method:** `POST`
- **Path:** `/queue/:id/items/:itemId/unresolve`
- **Base URL:** `https://api.moderationapi.com/v1`
- **Official documentation:** [Unresolve A Queue Item](https://docs.moderationapi.com/api-reference/review-queues/unresolve-a-queue-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The queue ID |
| `itemId` | path | `string` | yes | The item ID to unresolve |
| `comment` | body | `string` | no | Optional reason for unresolving the item |
