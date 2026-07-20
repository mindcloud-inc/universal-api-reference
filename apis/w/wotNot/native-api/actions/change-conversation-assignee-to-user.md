# Change Conversation Assignee To User with WotNot

Updates a conversation assignee to a user in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/events`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Change Conversation Assignee To User](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation ID |
| `user.by` | body | `string` | yes | Current assignee email |
| `user.to` | body | `string` | yes | New assignee email |
