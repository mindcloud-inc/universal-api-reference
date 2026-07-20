# List Tagged Posts with Tumblr

Retrieves Tumblr posts with a specific tag.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/tagged`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [List Tagged Posts](https://www.tumblr.com/docs/en/api/v2#tagged--get-posts-with-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | query | `string` | yes | The tag on the posts you'd like to retrieve. |
| `before` | query | `number` | no | Return posts before this timestamp. |
| `filter` | query | `list<string>` | no | Alternative post format to return. Accepted values: `raw`, `text`. |
