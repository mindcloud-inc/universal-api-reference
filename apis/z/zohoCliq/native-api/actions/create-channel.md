# Create Channel with Zoho Cliq

Creates a new channel in Zoho Cliq.

## Endpoint

- **Method:** `POST`
- **Path:** `/channels`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [Create Channel](https://www.zoho.com/cliq/help/restapi/v2/#Channels_Create_a_channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The channel name. |
| `description` | body | `string` | no | A short description for the channel. |
| `level` | body | `string` | yes | The channel level: organization, team, private, or external. |
| `invite_only` | body | `boolean` | no | When true, users can join only by invitation. |
| `team_ids[]` | body | `array<string>` | no | The team IDs to associate with a team channel. |
| `user_ids[]` | body | `array<string>` | no | The user IDs to add as channel participants. |
| `email_ids[]` | body | `array<string>` | no | The email addresses to add as channel participants. |
| `image_data` | body | `string` | no | The base64-encoded display image for the channel. |
| `config.reply_mode` | body | `string` | no | How replies should work in the channel: normal_reply, threads, or both. |
| `config.leave_join_info` | body | `string` | no | Whether join and leave events should be posted in the channel. |
| `config.add_remove_info` | body | `string` | no | Whether add and remove participant events should be posted in the channel. |
| `config.meeting_chat_type` | body | `string` | no | Where meeting messages should be posted: channel, thread, or host_choice. |
