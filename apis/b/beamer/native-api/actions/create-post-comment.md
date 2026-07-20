# Create Post Comment with Beamer

Creates a new post comment in Beamer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/posts/:postId/comments`
- **Base URL:** `https://api.getbeamer.com`
- **Official documentation:** [Create Post Comment](https://help.userflow.com/beamer/docs/beamer-api-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `postId` | path | `number` | yes |
| `text` | body | `string` | yes |
| `userId` | body | `string` | no |
| `userEmail` | body | `string` | no |
| `userFirstname` | body | `string` | no |
| `userLastname` | body | `string` | no |
