# Get Post Reaction By ID with Beamer

Retrieves a post reaction from Beamer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/posts/:postId/reactions/:reactionId`
- **Base URL:** `https://api.getbeamer.com`
- **Official documentation:** [Get Post Reaction By ID](https://help.userflow.com/beamer/docs/beamer-api-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `postId` | path | `number` | yes |
| `reactionId` | path | `number` | yes |
