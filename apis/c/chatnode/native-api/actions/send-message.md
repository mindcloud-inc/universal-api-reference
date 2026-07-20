# Send Message with Chatnode

## Endpoint

- **Method:** `POST`
- **Path:** `:botId`
- **Base URL:** `https://api.public.chatnode.ai/v1`
- **Official documentation:** [Send Message](https://www.chatnode.ai/docs/developer-guides/api/send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | The Chatnode agent id associated with the trained agent model. |
| `chat_session_id` | body | `string` | no | Optional chat session id to continue an existing conversation. |
| `message` | body | `string` | yes | The message to send to your agent. |
| `streaming` | body | `boolean` | no | Whether to enable streaming responses. Defaults to false. |
