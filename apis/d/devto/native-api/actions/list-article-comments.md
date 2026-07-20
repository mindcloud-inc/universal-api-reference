# List Article Comments with Dev.to

Lists threaded comments for a Dev.to article or podcast episode.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments`
- **Base URL:** `https://dev.to/api`
- **Official documentation:** [List Article Comments](https://developers.forem.com/api/v1#tag/comments/operation/getCommentsByArticleId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `a_id` | query | `string` | no | Article identifier to fetch comments for. |
| `p_id` | query | `string` | no | Podcast episode identifier to fetch comments for. |
