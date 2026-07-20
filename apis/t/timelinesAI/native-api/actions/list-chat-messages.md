# List Chat Messages with TimelinesAI

Retrieves messages from a specific TimelinesAI chat.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats/{chat_id}/messages`
- **Base URL:** `https://app.timelines.ai/integrations/api`
- **Official documentation:** [List Chat Messages](https://timelinesai.mintlify.app/public-api-reference/get-filtered-chat-history-messages-only-of-the-chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | path | `number` | yes | ID of the chat in TimelinesAI. You can find it in the chat URL or outbound webhook payload. |
| `from_me` | query | `boolean` | no | Filter messages sent from your WhatsApp account or received from others. |
| `after` | query | `date` | no | Filter messages created after this date or datetime. |
| `before` | query | `date` | no | Filter messages created before this date or datetime. |
| `after_message` | query | `string` | no | Filter messages created after the specified message UID. |
| `before_message` | query | `string` | no | Filter messages created before the specified message UID. |
| `sorting_order` | query | `string` | no | Order messages by timestamp using asc or desc. |
