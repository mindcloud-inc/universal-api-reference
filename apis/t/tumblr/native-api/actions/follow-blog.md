# Follow Blog with Tumblr

Follows a Tumblr blog from the user account.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/user/follow`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [Follow Blog](https://www.tumblr.com/docs/en/api/v2#userfollow--follow-a-blog)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | no | The URL of the blog to follow. |
| `email` | body | `string` | no | The email of the blog to follow when the blog can be found by email. |
