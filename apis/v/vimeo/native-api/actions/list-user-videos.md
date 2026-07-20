# List User Videos with Vimeo

Retrieves a user's uploaded videos from Vimeo.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:user_id/videos`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [List User Videos](https://developer.vimeo.com/api/reference/videos#get_videos)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | The ID of the user. |
| `query` | query | `string` | no | The search query to use to filter the results. |
| `query_fields` | query | `list` | no | The fields to search against. Accepted values: `chapters`, `description`, `tags`, `title`. Send multiple values as a string. |
| `filter` | query | `list` | no | The attribute by which to filter the results. Accepted values: `app_only`, `cold_storage`, `embeddable`, `featured`, `live`, `no_placeholder`, `nolive`, `playable`, `screen_recorded`. |
| `containing_uri` | query | `string` | no | Return only videos that contain the specified URI. |
| `filter_tag` | query | `string` | no | Return only videos with the specified tag. |
| `filter_tag_all_of` | query | `string` | no | Return only videos that contain all specified tags. |
| `filter_tag_exclude` | query | `string` | no | Return only videos that exclude the specified tag. |
| `filter_uploader` | query | `number` | no | Return only videos uploaded by the specified uploader ID. |
| `filter_embeddable` | query | `boolean` | no | Whether to filter by embeddable videos. |
| `filter_playable` | query | `boolean` | no | Whether to filter by playable videos. |
| `filter_screen_recorded` | query | `boolean` | no | Whether to filter by screen-recorded videos. |
