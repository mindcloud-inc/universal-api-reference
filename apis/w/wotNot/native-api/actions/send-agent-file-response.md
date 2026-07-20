# Send Agent File Response with WotNot

Creates an agent file message in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/messages`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Send Agent File Response](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation ID |
| `message.file.path` | body | `string` | yes | Public file URL |
| `message.file.size` | body | `number` | yes | File size in MB |
| `message.file.type` | body | `string` | yes | File MIME type |
| `message.file.name` | body | `string` | yes | Filename shown to the user |
| `user.by` | body | `string` | yes | Agent email sending the response |
