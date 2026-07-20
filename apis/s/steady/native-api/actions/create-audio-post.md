# Create Audio Post with Steady

Creates a new audio post in Steady.

## Endpoint

- **Method:** `POST`
- **Path:** `/posts/audio_posts`
- **Base URL:** `https://steadyhq.com/api/v1`
- **Official documentation:** [Create Audio Post](https://developers.steadyhq.com/#creating-a-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio_url` | body | `string` | yes | A URL ending in .mp3 or .m4a. |
| `content` | body | `string` | no | Optional post content. HTML is sanitized by Steady. |
| `description` | body | `string` | yes | The description of the post. |
| `distribute_as_email` | body | `boolean` | no | Optional boolean to send the post as email when published. |
| `distribute_on_steady_page` | body | `boolean` | no | Optional boolean to display the post on the Steady page. |
| `publish_at` | body | `date` | no | Optional future ISO8601 datetime to schedule publication. |
| `published_at` | body | `date` | no | Optional ISO8601 datetime for an already-published post. |
| `restrict_to_plan_ids` | body | `list<string>` | no | Optional list of plan IDs that can access the post. |
| `teaser_image` | body | `string` | no | Optional image URL used when displaying the post on Steady. |
| `title` | body | `string` | yes | The title of the post. |
