# Update Channel with Zoho Cliq

Updates an existing channel in Zoho Cliq.

## Endpoint

- **Method:** `PUT`
- **Path:** `/channels/:channelId`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [Update Channel](https://www.zoho.com/cliq/help/restapi/v2/#Channels_Update_a_channel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelId` | path | `string` | yes | The ID of the channel to update. |
| `name` | body | `string` | no | The updated channel name. |
| `description` | body | `string` | no | The updated channel description. |
| `image_data` | body | `string` | no | The updated base64-encoded display image for the channel. |
| `config.reply_mode` | body | `string` | no | How replies should work in the channel: normal_reply, threads, or both. |
| `config.leave_join_info` | body | `string` | no | Whether join and leave events should be posted in the channel. |
| `config.add_remove_info` | body | `string` | no | Whether add and remove participant events should be posted in the channel. |
| `config.meeting_chat_type` | body | `string` | no | Where meeting messages should be posted: channel, thread, or host_choice. |
