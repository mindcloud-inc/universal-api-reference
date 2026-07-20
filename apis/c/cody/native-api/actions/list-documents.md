# List Documents with Cody

## Endpoint

- **Method:** `GET`
- **Path:** `/documents`
- **Base URL:** `https://getcody.ai/api/v1`
- **Official documentation:** [List Documents](https://developers.meetcody.ai/operation/operation-list-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | query | `string` | no | Id of the folder to list documents for. |
| `conversation_id` | query | `string` | no | Id of the conversation to only list documents the conversation is focused on. |
| `keyword` | query | `string` | no | Keyword to filter the list to documents that partially match the name. |
