# List Last N Posts with TrackYourSocials

Retrieves the last N posts from a social profile in TrackYourSocials.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/last-n-posts`
- **Base URL:** `https://trackyoursocials.com`
- **Official documentation:** [List Last N Posts](https://trackyoursocials.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `n` | query | `number` | no | Number of posts to return. Supported range: 1 to 200. |
| `user_account` | query | `string` | yes | Profile URL or handle for the social media account. |
