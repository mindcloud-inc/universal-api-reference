# List Post Comments with Beamer

Retrieves comments for a post from Beamer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/posts/:postId/comments`
- **Base URL:** `https://api.getbeamer.com`
- **Official documentation:** [List Post Comments](https://help.userflow.com/beamer/docs/beamer-api-reference)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `postId` | path | `number` | yes |
| `dateFrom` | query | `string` | no |
| `dateTo` | query | `string` | no |
| `language` | query | `string` | no |
| `search` | query | `string` | no |
