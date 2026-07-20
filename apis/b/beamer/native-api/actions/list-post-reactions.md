# List Post Reactions with Beamer

Retrieves reactions for a post from Beamer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/posts/:postId/reactions`
- **Base URL:** `https://api.getbeamer.com`
- **Official documentation:** [List Post Reactions](https://help.userflow.com/beamer/docs/beamer-api-reference)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `postId` | path | `number` | yes |
| `dateFrom` | query | `string` | no |
| `dateTo` | query | `string` | no |
| `reaction` | query | `string` | no |
