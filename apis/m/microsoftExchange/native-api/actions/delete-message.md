# Delete Message with Microsoft Exchange

Deletes a message from Microsoft Exchange.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1.0/me/messages/{{messageId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Delete Message](https://learn.microsoft.com/en-us/graph/api/message-delete?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The ID of the Exchange message to delete. |
