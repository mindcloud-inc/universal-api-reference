# Update Chat Settings with Twitch

Updates channel chat settings in Twitch.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/chat/settings`
- **Base URL:** `https://api.twitch.tv/helix`
- **Official documentation:** [Update Chat Settings](https://dev.twitch.tv/docs/api/reference#update-chat-settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcaster_id` | query | `string` | yes | The ID of the broadcaster whose chat settings you want to update. |
| `moderator_id` | query | `string` | yes | The ID of the moderator making the update. |
| `emote_mode` | body | `boolean` | no | Whether chat messages must contain only emotes. |
| `follower_mode` | body | `boolean` | no | Whether the broadcaster restricts the chat room to followers only. |
| `follower_mode_duration` | body | `number` | no | How long, in minutes, users must follow before chatting. |
| `non_moderator_chat_delay` | body | `boolean` | no | Whether to delay non-moderator messages before showing them in chat. |
| `non_moderator_chat_delay_duration` | body | `number` | no | The number of seconds to delay non-moderator chat messages. |
| `slow_mode` | body | `boolean` | no | Whether to limit how often users may send messages. |
| `slow_mode_wait_time` | body | `number` | no | The number of seconds users must wait between messages. |
| `subscriber_mode` | body | `boolean` | no | Whether only subscribers may chat. |
| `unique_chat_mode` | body | `boolean` | no | Whether only unique chat messages are allowed. |
