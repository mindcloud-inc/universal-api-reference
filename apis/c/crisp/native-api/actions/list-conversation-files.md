# List Conversation Files with Crisp

Retrieves files for a Crisp conversation.

## Endpoint

- **Method:** `GET`
- **Path:** `/website/:website_id/conversation/:session_id/files/:page_number`
- **Base URL:** `https://api.crisp.chat/v1`
- **Official documentation:** [List Conversation Files](https://docs.crisp.chat/references/rest-api/v1/#list-conversation-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website_id` | path | `string` | yes | The website identifier |
| `session_id` | path | `string` | yes | The conversation session identifier |
| `page_number` | path | `number` | no | The page number for file list paging |
