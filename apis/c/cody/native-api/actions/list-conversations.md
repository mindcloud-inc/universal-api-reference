# List Conversations with Cody

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations`
- **Base URL:** `https://getcody.ai/api/v1`
- **Official documentation:** [List Conversations](https://developers.meetcody.ai/operation/operation-list-conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | query | `list<string>` | no | Id of the bot to filter the list of conversations to only those that are using the selected bot. |
| `keyword` | query | `string` | no | Keyword to filter the list of conversations to only those that at least partially match the conversation name. |
| `includes` | query | `list<string>` | no | Lists document ids the conversation is focused on. Accepted values: `document_ids`. |
