# Send Draft Message with Microsoft 365

Sends a draft message from Microsoft 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/messages/{{messageId}}/send`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Send Draft Message](https://learn.microsoft.com/en-us/graph/api/message-send?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The ID of the draft message to send. |
