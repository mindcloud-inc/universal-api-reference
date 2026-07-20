# Forward Message with Microsoft 365

Forwards a message from Microsoft 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/messages/{{messageId}}/forward`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Forward Message](https://learn.microsoft.com/en-us/graph/api/message-forward?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The ID of the Outlook message to forward. |
| `toRecipients[].emailAddress.address` | body | `string` | no | The email address to forward the message to. |
| `comment` | body | `string` | no | Optional text to include above the forwarded message. |
