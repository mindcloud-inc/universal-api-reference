# Get Conversation with Cody

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations/:id`
- **Base URL:** `https://getcody.ai/api/v1`
- **Official documentation:** [Get Conversation](https://developers.meetcody.ai/operation/operation-get-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Id of the conversation. |
| `includes` | query | `list<string>` | no | Lists document ids the conversation is focused on. Accepted values: `document_ids`. |
