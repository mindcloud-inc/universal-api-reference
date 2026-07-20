# Create Conversation with Cody

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations`
- **Base URL:** `https://getcody.ai/api/v1`
- **Official documentation:** [Create Conversation](https://developers.meetcody.ai/operation/operation-create-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Conversation name. |
| `bot_id` | body | `list<string>` | yes | Id of the bot to use for the conversation. |
| `document_ids[]` | body | `array<string>` | no | Document ids the conversation should focus on. |
