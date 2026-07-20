# Close Conversation with WotNot

Closes a conversation in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/events`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Close Conversation](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation ID |
| `user.by` | body | `string` | yes | Agent email closing the conversation |
