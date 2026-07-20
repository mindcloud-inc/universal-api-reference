# Edit Comment Metadata with Liveblocks

Updates comment metadata in Liveblocks.

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/:roomId/threads/:threadId/comments/:commentId/metadata`
- **Base URL:** `https://api.liveblocks.io/v2`
- **Official documentation:** [Edit Comment Metadata](https://liveblocks.io/docs/api-reference/rest-api-endpoints#edit-comment-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentId` | path | `string` | no | ID of the comment. |
| `metadata` | body | `object` | no | — |
| `roomId` | path | `string` | no | — |
| `threadId` | path | `string` | no | — |
| `updatedAt` | body | `string` | no | — |
| `userId` | body | `string` | no | — |
