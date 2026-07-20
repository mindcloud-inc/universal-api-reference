# Get Message Hook with Landbot

Retrieves a message hook from a Landbot channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/channels/:channel_id/message_hooks/:hook_id/`
- **Base URL:** `https://api.landbot.io`
- **Official documentation:** [Get Message Hook](https://api.landbot.io/#api-MessageHooks-GetHttpsApiLandbotIoV1ChannelsChannel_idMessage_hooksHook_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id` | path | `number` | yes | Channel ID that owns the hook. |
| `hook_id` | path | `number` | yes | Hook ID to retrieve. |
