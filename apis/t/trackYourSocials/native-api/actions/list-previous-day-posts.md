# List Previous Day Posts with TrackYourSocials

Retrieves yesterday's posts from a social media channel in TrackYourSocials.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/previous-day-posts`
- **Base URL:** `https://trackyoursocials.com`
- **Official documentation:** [List Previous Day Posts](https://trackyoursocials.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_account` | query | `string` | yes | URL of the social media channel to fetch yesterday's posts from. |
