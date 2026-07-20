# List Posts with Pinboard

## Endpoint

- **Method:** `GET`
- **Path:** `/posts/get`
- **Base URL:** `https://api.pinboard.in/v1`
- **Official documentation:** [List Posts](https://pinboard.in/api/#posts_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dt` | query | `date` | no | Return results bookmarked on this day. |
| `meta` | query | `boolean` | no | Include change detection metadata. |
| `tag` | query | `string` | no | Filter by up to three tags. |
| `url` | query | `string` | no | Return the bookmark for this URL. |
