# List All Posts with Pinboard

## Endpoint

- **Method:** `GET`
- **Path:** `/posts/all`
- **Base URL:** `https://api.pinboard.in/v1`
- **Official documentation:** [List All Posts](https://pinboard.in/api/#posts_all)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromdt` | query | `date` | no | Return bookmarks created after this time. |
| `meta` | query | `boolean` | no | Include change detection metadata. |
| `results` | query | `number` | no | Number of results to return. |
| `start` | query | `number` | no | Offset value. |
| `tag` | query | `string` | no | Filter by up to three tags. |
| `todt` | query | `date` | no | Return bookmarks created before this time. |
