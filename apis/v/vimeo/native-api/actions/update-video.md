# Update Video with Vimeo

Updates an existing video in Vimeo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/videos/:video_id`
- **Base URL:** `https://api.vimeo.com`
- **Official documentation:** [Update Video](https://developer.vimeo.com/api/reference/videos#edit_video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `video_id` | path | `number` | yes | The ID of the video. |
| `name` | body | `string` | no | The title of the video. This field can hold a maximum of 128 characters. |
| `description` | body | `string` | no | The description of the video. This field can hold a maximum of 5000 characters. |
| `privacy.view` | body | `list` | no | The video's privacy setting. Accepted values: `anybody`, `contacts`, `disable`, `nobody`, `password`, `team`, `unlisted`, `users`. |
| `content_rating[]` | body | `array<string>` | no | A list of values describing the content in this video. |
| `custom_url` | body | `string` | no | The custom link of the video. |
| `hide_from_vimeo` | body | `boolean` | no | Whether to hide the video from everyone except the video's owner. |
| `license` | body | `list` | no | The Creative Commons license under which the video is offered. Accepted values: `by`, `by-nc`, `by-nc-nd`, `by-nc-sa`, `by-nd`, `by-sa`, `cc0`. |
| `locale` | body | `string` | no | The video's default language. |
| `privacy.add` | body | `boolean` | no | Whether a user can add the video to a showcase, channel, or group. |
| `privacy.comments` | body | `list` | no | The privacy level required to comment on the video. Accepted values: `anybody`, `contacts`, `nobody`. |
| `privacy.download` | body | `boolean` | no | Whether a user can download the video. |
| `privacy.embed` | body | `list` | no | The video's embed setting. Accepted values: `private`, `public`, `whitelist`. |
| `review_page.active` | body | `boolean` | no | Whether to enable video review. |
