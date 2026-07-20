# Delete Post Reaction with Beamer

Deletes a post reaction from Beamer.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v0/posts/:postId/reactions/:reactionId`
- **Base URL:** `https://api.getbeamer.com`
- **Official documentation:** [Delete Post Reaction](https://help.userflow.com/beamer/docs/beamer-api-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `postId` | path | `number` | yes |
| `reactionId` | path | `number` | yes |
