# Create Message Hook with Landbot

Creates a message hook for a Landbot channel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/channels/:channel_id/message_hooks/`
- **Base URL:** `https://api.landbot.io`
- **Official documentation:** [Create Message Hook](https://api.landbot.io/#api-MessageHooks-PostHttpsApiLandbotIoV1ChannelsChannel_idMessage_hooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id` | path | `number` | yes | Channel ID where the hook will be created. |
| `url` | body | `string` | yes | Webhook URL for incoming message notifications. |
| `token` | body | `string` | no | Optional token Landbot will send with the hook. |
| `name` | body | `string` | no | Optional display name for the hook. |
