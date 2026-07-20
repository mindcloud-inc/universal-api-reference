# Count Post Reactions with Beamer

Retrieves a post reaction count from Beamer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/posts/:postId/reactions/count`
- **Base URL:** `https://api.getbeamer.com`
- **Official documentation:** [Count Post Reactions](https://help.userflow.com/beamer/docs/beamer-api-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `postId` | path | `number` | yes |
| `dateFrom` | query | `string` | no |
| `dateTo` | query | `string` | no |
| `reaction` | query | `string` | no |
