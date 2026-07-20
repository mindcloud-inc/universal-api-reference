# Create Draft Message with Microsoft 365

Creates a draft message in Microsoft 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/messages`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Create Draft Message](https://learn.microsoft.com/en-us/graph/api/user-post-messages?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `toRecipients[].emailAddress.address` | body | `string` | no | The email address to add as the draft recipient. |
| `subject` | body | `string` | no | The draft email subject line. |
| `body.content` | body | `string` | no | The draft email body content. |
