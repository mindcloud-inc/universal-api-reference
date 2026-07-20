# Send Message with Cody

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `https://getcody.ai/api/v1`
- **Official documentation:** [Send Message](https://developers.meetcody.ai/operation/operation-send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Message content, up to 2000 characters. |
| `conversation_id` | body | `string` | yes | Id of the conversation to send the message to. |
