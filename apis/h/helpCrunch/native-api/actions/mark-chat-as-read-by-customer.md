# Mark Chat As Read By Customer with HelpCrunch

Marks a chat as read by a customer in HelpCrunch.

## Endpoint

- **Method:** `PUT`
- **Path:** `/chats/readByCustomer`
- **Base URL:** `https://api.helpcrunch.com/v1`
- **Official documentation:** [Mark Chat As Read By Customer](https://docs.helpcrunch.com/en/rest-api-v1/read-chat-rest-api-1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `number` | yes |
| `read` | body | `boolean` | yes |
