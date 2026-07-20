# Reassign Conversation To Team with QWIC

Reassigns a QWIC conversation to a team.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/events`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Reassign Conversation To Team](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#changing-assignee-in-a-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | The QWIC conversation identifier. |
| `team.by` | body | `string` | yes | The current team identifier. |
| `team.to` | body | `string` | yes | The target team identifier. |
