# Create Reply Draft with Microsoft 365 Outlook

Creates a draft reply to a message in Microsoft 365 Outlook, without sending it. The draft is pre-addressed to the original sender. Use Update Draft Message to change recipients, CC, subject, or body, then Send Draft Message to send it.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/messages/{{messageId}}/createReply`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create Reply Draft](https://learn.microsoft.com/en-us/graph/api/message-createreply?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The ID of the Outlook message to create a reply draft for. |
