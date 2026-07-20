# Like Post with Tumblr

Likes a Tumblr post from the user account.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/user/like`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [Like Post](https://www.tumblr.com/docs/en/api/v2#userlike--like-a-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The ID of the post to like. |
| `reblog_key` | body | `string` | yes | The reblog key for the post. |
