# Count Post Comments with Beamer

Retrieves a post comment count from Beamer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/posts/:postId/comments/count`
- **Base URL:** `https://api.getbeamer.com`
- **Official documentation:** [Count Post Comments](https://help.userflow.com/beamer/docs/beamer-api-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `postId` | path | `number` | yes |
| `dateFrom` | query | `string` | no |
| `dateTo` | query | `string` | no |
| `language` | query | `string` | no |
| `search` | query | `string` | no |
