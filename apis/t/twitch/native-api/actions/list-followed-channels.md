# List Followed Channels with Twitch

Retrieves followed channels for a user from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/followed`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [List Followed Channels](https://dev.twitch.tv/docs/api/reference#get-followed-channels)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | query | `string` | yes | Returns broadcasters followed by this user. This ID must match the user ID in the user OAuth token. |
| `broadcaster_id` | query | `string` | no | Filters the response to a specific broadcaster to check whether the user follows them. |
| `first` | query | `number` | no | Maximum number of followed channels to return. Minimum 1, maximum 100. |
| `after` | query | `string` | no | Cursor for the next page of followed channels. |
