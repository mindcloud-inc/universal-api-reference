# Reassign Conversation To Agent with QWIC

Reassigns a QWIC conversation to an agent.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/events`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Reassign Conversation To Agent](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#changing-assignee-in-a-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | The QWIC conversation identifier. |
| `user.by` | body | `string` | yes | The current assignee email address. |
| `user.to` | body | `string` | yes | The target assignee email address. |
