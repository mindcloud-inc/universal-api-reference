# Send Visitor Response with QWIC

Sends a visitor response to a QWIC conversation.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/messages`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Send Visitor Response](https://qwic-1.gitbook.io/help/deploying-agents/publishing-agents/api#send-visitor-response)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | QWIC conversation ID. |
| `message` | body | `object` | yes | Visitor text response message object. |
