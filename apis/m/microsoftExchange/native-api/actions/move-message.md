# Move Message with Microsoft Exchange

Moves a message to another folder in Microsoft Exchange.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/messages/{{messageId}}/move`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Move Message](https://learn.microsoft.com/en-us/graph/api/message-move?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The ID of the Exchange message to move. |
| `destinationId` | body | `string` | yes | The destination folder ID or a well-known Exchange folder name such as deleteditems or archive. |
