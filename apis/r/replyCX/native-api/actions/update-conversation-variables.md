# Update Conversation Variables with ReplyCX

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/accounts/:account_id/conversations/:conversation_id/variables`
- **Base URL:** `https://api.reply.cx`
- **Official documentation:** [Update Conversation Variables](https://help.reply.cx/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | — |
| `variables` | body | `list<object>` | yes | List of variable objects with keys name, type, and value. |
