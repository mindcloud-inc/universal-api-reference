# Get Posts with Stackoverflow

Retrieves specific posts from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/posts/[:ids]`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [Get Posts](https://api.stackexchange.com/docs/posts-by-ids)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | path | `string` | yes | Semicolon-separated Stack Exchange post IDs. |
| `site` | query | `string` | yes | Stack Exchange site parameter, for example stackoverflow. |
