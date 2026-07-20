# Add Bookmark with Pinboard

## Endpoint

- **Method:** `GET`
- **Path:** `/posts/add`
- **Base URL:** `https://api.pinboard.in/v1`
- **Official documentation:** [Add Bookmark](https://pinboard.in/api/#posts_add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | query | `string` | yes | Title of the bookmarked page. |
| `dt` | query | `date` | no | Bookmark creation time. |
| `extended` | query | `string` | no | Longer description for the bookmark. |
| `replace` | query | `boolean` | no | Replace an existing bookmark for the same URL. |
| `shared` | query | `boolean` | no | Make the bookmark public. |
| `tags` | query | `string` | no | Whitespace-separated tags. |
| `toread` | query | `boolean` | no | Mark the bookmark as unread. |
| `url` | query | `string` | yes | The URL to bookmark. |
