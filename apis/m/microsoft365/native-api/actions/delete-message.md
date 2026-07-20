# Delete Message with Microsoft 365

Deletes a message from Microsoft 365.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1.0/me/messages/{{messageId}}`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Delete Message](https://learn.microsoft.com/en-us/graph/api/message-delete?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The ID of the Outlook message to delete. |
