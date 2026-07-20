# Move Message with Microsoft 365 Outlook

Moves a message to another mail folder in Microsoft 365 Outlook.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/messages/{{messageId}}/move`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Move Message](https://learn.microsoft.com/en-us/graph/api/message-move?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The ID of the Outlook message to move. |
| `destinationId` | body | `string` | yes | The destination folder ID or a well-known Outlook folder name such as deleteditems or archive. |
