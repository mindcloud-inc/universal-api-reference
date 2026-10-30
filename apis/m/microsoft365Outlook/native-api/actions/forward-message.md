# Forward Message with Microsoft 365 Outlook

Forwards a message from Microsoft 365 Outlook.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/messages/{{messageId}}/forward`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Forward Message](https://learn.microsoft.com/en-us/graph/api/message-forward?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The ID of the Outlook message to forward. |
| `toRecipients` | body | `string` | yes | Comma-separated email addresses to forward the message to. Example: person@example.com, other@example.com |
| `comment` | body | `string` | no | Optional text to include above the forwarded message. |
