# Update Draft Message with Microsoft 365

Updates a draft message in Microsoft 365.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1.0/me/messages/{{messageId}}`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Update Draft Message](https://learn.microsoft.com/en-us/graph/api/message-update?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | path | `string` | yes | The ID of the Outlook message to update. |
| `subject` | body | `string` | no | Updated message subject. This is most useful when editing a draft message. |
| `body.content` | body | `string` | no | Updated message body content. This is most useful when editing a draft message. |
