# Create Conversation with Intercom

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations`
- **Base URL:** `https://api.intercom.io`
- **Official documentation:** [Create Conversation](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/conversations/createconversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `object` | no | — |
| `from.id` | body | `string` | yes | Intercom user contact ID |
| `body` | body | `string` | yes | Conversation message body |
