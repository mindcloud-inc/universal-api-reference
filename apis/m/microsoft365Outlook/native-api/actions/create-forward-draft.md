# Create Forward Draft with Microsoft 365 Outlook

Creates a draft forward of a message in Microsoft 365 Outlook, without sending it. Use Update Draft Message to change recipients, CC, subject, or body, then Send Draft Message to send it.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/messages/{{messageId}}/createForward`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create Forward Draft](https://learn.microsoft.com/en-us/graph/api/message-createforward?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The ID of the Outlook message to create a forward draft for. |
| `toRecipients` | body | `string` | yes | Comma-separated email addresses to forward the draft to. Example: person@example.com, other@example.com |
| `comment` | body | `string` | no | Optional text to include above the forwarded message. |
