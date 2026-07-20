# Schedule Post with Tailwind

Schedules an existing post in Tailwind.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/:accountId/posts/:postId/schedule`
- **Base URL:** `https://api-v1.tailwind.ai`
- **Official documentation:** [Schedule Post](https://api-docs.tailwind.ai/rest-api/operations/v1accountsaccountidpostspostidschedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Pinterest account ID. |
| `postId` | path | `string` | yes | Tailwind post ID. |
| `sendAt` | body | `date` | yes | ISO 8601 time when the post should be published. |
| `boardId` | body | `string` | no | Target board ID. Required when scheduling a draft that does not already have a board. |
