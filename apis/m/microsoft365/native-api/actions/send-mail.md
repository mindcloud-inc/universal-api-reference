# Send Mail with Microsoft 365

Sends an email from Microsoft 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/sendMail`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Send Mail](https://learn.microsoft.com/en-us/graph/api/user-sendmail?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message.toRecipients[].emailAddress.address` | body | `string` | no | The recipient email address. |
| `message.subject` | body | `string` | no | The email subject line. |
| `message.body.content` | body | `string` | no | The text content of the email body. |
