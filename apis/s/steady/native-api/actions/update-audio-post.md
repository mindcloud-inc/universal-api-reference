# Update Audio Post with Steady

Updates an existing audio post in Steady.

## Endpoint

- **Method:** `PUT`
- **Path:** `/posts/audio_posts/:post_id`
- **Base URL:** `https://steadyhq.com/api/v1`
- **Official documentation:** [Update Audio Post](https://developers.steadyhq.com/#updating-a-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio_url` | body | `string` | no | A URL ending in .mp3 or .m4a. |
| `content` | body | `string` | no | Optional post content. HTML is sanitized by Steady. |
| `description` | body | `string` | no | The description of the post. |
| `distribute_as_email` | body | `boolean` | no | Optional boolean to send the post as email when published. |
| `distribute_on_steady_page` | body | `boolean` | no | Optional boolean to display the post on the Steady page. |
| `post_id` | path | `string` | yes | The ID of the audio post to update. |
| `publish_at` | body | `date` | no | Optional future ISO8601 datetime to schedule publication when the post is not yet published. |
| `restrict_to_plan_ids` | body | `list<string>` | no | Optional list of plan IDs that can access the post. |
| `teaser_image` | body | `string` | no | Optional image URL used when displaying the post on Steady. |
| `title` | body | `string` | no | The title of the post. |
