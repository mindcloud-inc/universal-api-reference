# Create Ticket Conversation with SuperOps IT

## Endpoint

- **Method:** `POST`
- **Path:** `/it`
- **Base URL:** `https://api.superops.ai`
- **Official documentation:** [Create Ticket Conversation](https://developer.superops.com/it#mutation-createTicketConversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ticketId` | body | `string` | yes | The SuperOps ticket ID. |
| `content` | body | `string` | yes | The conversation content. |
| `userId` | body | `string` | no | Optional user ID creating the conversation. |
| `time` | body | `date` | no | Optional conversation creation time in ISO 8601 format. |
| `sendMail` | body | `boolean` | no | Whether SuperOps should send mail for the conversation. |
