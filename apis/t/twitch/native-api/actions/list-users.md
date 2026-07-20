# List Users with Twitch

Retrieves user profiles and metadata from Twitch.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [List Users](https://dev.twitch.tv/docs/api/reference#get-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | Twitch user ID to look up. |
| `login` | query | `string` | no | Twitch login name to look up. |
