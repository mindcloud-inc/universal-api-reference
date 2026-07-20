# Mark Events As Seen with LiveChat

Updates chat events as seen in LiveChat.

## Endpoint

- **Method:** `POST`
- **Path:** `/mark_events_as_seen`
- **Base URL:** `https://api.livechatinc.com/v3.6/agent/action`
- **Official documentation:** [Mark Events As Seen](https://platform.text.com/docs/messaging/agent-chat-api#mark-events-as-seen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | body | `string` | yes | The chat ID. |
| `seen_up_to` | body | `date` | yes | RFC3339 timestamp marking the newest seen event. |
