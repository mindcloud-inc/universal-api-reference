# Update Chat with TimelinesAI

Updates an existing chat in TimelinesAI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/chats/{chat_id}`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [Update Chat](https://timelinesai.mintlify.app/public-api-reference/update-chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | path | `number` | yes | ID of the chat in TimelinesAI. You can find it in the chat URL or outbound webhook payload. |
| `name` | body | `string` | no | Unique chat name in the workspace. |
| `responsible` | body | `string` | no | Email address of the teammate to assign, or an empty string to unassign. |
| `closed` | body | `boolean` | no | Set the chat to closed or open. |
| `read` | body | `boolean` | no | Set the chat to read or unread. |
| `chatgpt_autoresponse_enabled` | body | `boolean` | no | Enable or disable ChatGPT autoresponse for the chat. |
