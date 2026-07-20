# List Recent Posts with Pinboard

## Endpoint

- **Method:** `GET`
- **Path:** `/posts/recent`
- **Base URL:** `https://api.pinboard.in/v1`
- **Official documentation:** [List Recent Posts](https://pinboard.in/api/#posts_recent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | no | Number of results to return. |
| `tag` | query | `string` | no | Filter by up to three tags. |
