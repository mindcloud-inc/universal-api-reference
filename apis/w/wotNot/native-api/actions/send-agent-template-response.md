# Send Agent Template Response with WotNot

Creates an agent template message in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/messages`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Send Agent Template Response](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation ID |
| `message.data.template` | body | `string` | yes | Approved template name |
| `user.by` | body | `string` | yes | Agent email sending the response |
