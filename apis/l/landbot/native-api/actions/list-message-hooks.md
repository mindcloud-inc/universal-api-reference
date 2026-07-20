# List Message Hooks with Landbot

Retrieves message hooks for a Landbot channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/channels/:channel_id/message_hooks/`
- **Base URL:** `https://api.landbot.io`
- **Official documentation:** [List Message Hooks](https://api.landbot.io/#api-MessageHooks-GetHttpsApiLandbotIoV1ChannelsChannel_idMessage_hooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_id` | path | `number` | yes | Channel ID whose message hooks to list. |
