# Modify Channel Information with Twitch

Updates broadcaster channel information in Twitch.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/channels`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [Modify Channel Information](https://dev.twitch.tv/docs/api/reference#modify-channel-information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | The broadcaster whose channel to update. This ID must match the user ID in the access token. |
| `game_id` | body | `string` | no | Updates the active game/category. Use 0 or an empty string to unset the game. |
| `broadcaster_language` | body | `string` | no | ISO 639-1 language code for the stream, or other when Twitch does not support the language. |
| `title` | body | `string` | no | Updates the stream title. Twitch does not allow an empty title. |
| `delay` | body | `string` | no | Broadcast delay in seconds. Only Partner channels may set this value. Maximum 900. |
| `tags` | body | `string` | no | Channel-defined tags to apply. Maximum 10 tags; each tag is limited to 25 characters and may not contain spaces or special characters. |
| `content_classification_labels[].id` | body | `string` | no | Content Classification Label to enable or disable on the channel. |
