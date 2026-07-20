# Convert Conversation To Ticket with Intercom

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/:conversation_id/convert`
- **Base URL:** `https://api.intercom.io`
- **Official documentation:** [Convert Conversation To Ticket](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/convertconversationtoticket)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation_id` | path | `string` | yes | Intercom conversation identifier |
| `ticket_type_id` | body | `string` | yes | Intercom ticket type identifier |
| `ticket_attributes` | body | `object` | no | — |
| `ticket_attributes._default_title_` | body | `string` | no | Default converted ticket title |
| `ticket_attributes._default_description_` | body | `string` | no | Default converted ticket description |
