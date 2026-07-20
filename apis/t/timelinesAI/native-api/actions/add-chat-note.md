# Add Chat Note with TimelinesAI

Creates a note on an existing TimelinesAI chat.

## Endpoint

- **Method:** `POST`
- **Path:** `/chats/{chat_id}/notes`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [Add Chat Note](https://timelinesai.mintlify.app/public-api-reference/add-a-note-to-existing-chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | path | `number` | yes | ID of the chat in TimelinesAI. You can find it in the chat URL or outbound webhook payload. |
| `text` | body | `string` | yes | Note text to add to the chat. |
| `is_private` | body | `boolean` | no | Mark the note as private or visible to teammates. |
