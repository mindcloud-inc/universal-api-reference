# Get Customer Conversation with ThriveDesk

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/customer/conversations/{{conversationId}}`
- **Base URL:** `https://api.thrivedesk.com`
- **Official documentation:** [Get Customer Conversation](https://help.thrivedesk.com/en/wpportal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | ThriveDesk customer conversation ID. |
| `customer_email` | query | `string` | yes | Customer email address for the conversation lookup. |
