# List Contacts with Chatling

Retrieves contacts from Chatling.

## Endpoint

- **Method:** `GET`
- **Path:** `/chatbots/:chatbotId/contacts`
- **Base URL:** `https://api.chatling.ai/v2`
- **Official documentation:** [List Contacts](https://docs.chatling.ai/api-reference/v2/contacts/list-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatbotId` | path | `string` | yes | The chatbot ID. |
| `sort` | query | `string` | no | The sort order for the contacts list. |
