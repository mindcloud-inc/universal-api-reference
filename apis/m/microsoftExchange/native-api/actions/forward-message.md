# Forward Message with Microsoft Exchange

Forwards a message from Microsoft Exchange.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/messages/{{messageId}}/forward`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Forward Message](https://learn.microsoft.com/en-us/graph/api/message-forward?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The ID of the Exchange message to forward. |
| `toRecipients[].emailAddress.address` | body | `string` | no | The email address to forward the message to. |
| `comment` | body | `string` | no | Optional text to include above the forwarded message. |
