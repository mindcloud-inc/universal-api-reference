# Reply To Customer Conversation with ThriveDesk

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/customer/conversations/{{conversationId}}/reply`
- **Base URL:** `https://api.thrivedesk.com`
- **Official documentation:** [Reply To Customer Conversation](https://help.thrivedesk.com/en/wpportal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | ThriveDesk customer conversation ID to reply to. |
| `customer_email` | query | `string` | yes | Customer email address for the conversation reply. |
| `message` | body | `string` | yes | Reply message body. |
