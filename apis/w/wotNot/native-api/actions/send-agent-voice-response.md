# Send Agent Voice Response with WotNot

Creates an agent voice message in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/messages`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Send Agent Voice Response](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation ID |
| `message.file.path` | body | `string` | yes | Public voice file URL |
| `message.file.size` | body | `number` | yes | Voice file size in MB |
| `message.file.type` | body | `string` | yes | Voice file MIME type |
| `message.file.name` | body | `string` | yes | Voice filename |
| `user.by` | body | `string` | yes | Agent email sending the response |
