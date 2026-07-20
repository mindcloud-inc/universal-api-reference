# Update Conversation with Cody

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:id`
- **Base URL:** `https://getcody.ai/api/v1`
- **Official documentation:** [Update Conversation](https://developers.meetcody.ai/operation/operation-update-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Id of the conversation. |
| `name` | body | `string` | yes | Conversation name. |
| `bot_id` | body | `list<string>` | yes | Id of the bot to use for the conversation. |
| `document_ids[]` | body | `array<string>` | no | Document ids the conversation should focus on. |
