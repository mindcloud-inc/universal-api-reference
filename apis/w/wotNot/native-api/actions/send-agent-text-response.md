# Send Agent Text Response with WotNot

Creates an agent text message in WotNot.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/conversation/:conversation_id/messages`
- **Base URL:** `https://api.wotnot.io`
- **Official documentation:** [Send Agent Text Response](https://help.wotnot.io/build/integrations/public-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Conversation ID |
| `message.data.body` | body | `string` | yes | Message text to send |
| `user.by` | body | `string` | yes | Agent email sending the response |
