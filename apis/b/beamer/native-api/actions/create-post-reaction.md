# Create Post Reaction with Beamer

Creates a post reaction in Beamer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/posts/:postId/reactions`
- **Base URL:** `https://api.getbeamer.com`
- **Official documentation:** [Create Post Reaction](https://help.userflow.com/beamer/docs/beamer-api-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `postId` | path | `number` | yes |
| `reaction` | body | `string` | yes |
| `userId` | body | `string` | no |
| `userEmail` | body | `string` | no |
| `userFirstname` | body | `string` | no |
| `userLastname` | body | `string` | no |
