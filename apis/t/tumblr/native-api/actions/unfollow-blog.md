# Unfollow Blog with Tumblr

Unfollows a Tumblr blog from the user account.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/user/unfollow`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [Unfollow Blog](https://www.tumblr.com/docs/en/api/v2#userunfollow--unfollow-a-blog)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The URL of the blog to unfollow. |
