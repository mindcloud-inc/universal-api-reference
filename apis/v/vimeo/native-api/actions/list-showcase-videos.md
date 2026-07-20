# List Showcase Videos with Vimeo

Retrieves videos in a Vimeo showcase.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:user_id/albums/:album_id/videos`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [List Showcase Videos](https://developer.vimeo.com/api/reference/showcases#get_showcase_videos)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | The ID of the user. |
| `album_id` | path | `number` | yes | The ID of the showcase. |
| `query` | query | `string` | no | The search query to use to filter the results. |
| `sort` | query | `list<string>` | no | The way to sort the results. Accepted values: `alphabetical`, `comments`, `date`, `default`, `duration`, `likes`, `manual`, `modified_time`, `plays`. |
| `direction` | query | `list<string>` | no | The sort direction of the results. Accepted values: `asc`, `desc`. |
| `filter` | query | `list<string>` | no | The attribute by which to filter the results. Accepted values: `embeddable`, `playable`. |
| `filter_embeddable` | query | `boolean` | no | Whether to filter by embeddable videos when filter is embeddable. |
| `containing_uri` | query | `string` | no | The page containing the video URI. |
| `password` | query | `string` | no | The password of the showcase. |
| `weak_search` | query | `boolean` | no | Whether to include private videos in the search. |
