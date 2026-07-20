# List Published Articles with Dev.to

Lists published articles in Dev.to.

## Endpoint

- **Method:** `GET`
- **Path:** `/articles`
- **Base URL:** `https://dev.to/api`
- **Official documentation:** [List Published Articles](https://developers.forem.com/api/v1#tag/articles/operation/getArticles)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `state` | query | `string` | no | Article feed state: fresh, rising, or all. |
| `tag` | query | `string` | no | Return articles that contain this tag. |
| `tags` | query | `string` | no | Comma-separated tags; articles matching any tag are returned. |
| `tags_exclude` | query | `string` | no | Comma-separated tags to exclude. |
| `username` | query | `string` | no | User or organization username to filter articles. |
| `top` | query | `number` | no | Return popular articles from the last N days. |
| `collection_id` | query | `number` | no | Collection identifier to filter articles. |
