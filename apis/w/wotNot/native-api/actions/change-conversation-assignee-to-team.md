# Change Conversation Assignee To Team with WotNot

Updates a conversation assignee to a team in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/events`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Change Conversation Assignee To Team](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation ID |
| `team.by` | body | `string` | yes | Current assignee email |
| `team.to` | body | `string` | yes | Existing target team name |
