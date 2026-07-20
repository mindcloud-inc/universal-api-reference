# Send Message for Stream with Cody

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/stream`
- **Base URL:** `https://getcody.ai/api/v1`
- **Official documentation:** [Send Message for Stream](https://developers.meetcody.ai/operation/operation-send-message-for-stream)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | Message content, up to 2000 characters. |
| `conversation_id` | body | `string` | no | Id of the conversation to send the message to. |
| `redirect` | body | `boolean` | no | When true, Cody redirects to the SSE stream URL instead of returning it in JSON. |
