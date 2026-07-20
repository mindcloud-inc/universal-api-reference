# Unlike Post with Tumblr

Removes a like from a Tumblr post.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/user/unlike`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [Unlike Post](https://www.tumblr.com/docs/en/api/v2#userunlike--unlike-a-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The ID of the post to unlike. |
| `reblog_key` | body | `string` | yes | The reblog key for the post. |
