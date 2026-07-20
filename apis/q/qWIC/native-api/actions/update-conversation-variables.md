# Update Conversation Variables with QWIC

Updates variables for a QWIC conversation.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/:account_id/conversations/:conversation_id/variables`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Update Conversation Variables](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#update-variable-of-a-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | QWIC account ID. |
| `conversation_id` | path | `string` | yes | Conversation ID to update. |
| `variables` | body | `list<object>` | yes | Conversation/contact variable updates from the QWIC public API docs. |
