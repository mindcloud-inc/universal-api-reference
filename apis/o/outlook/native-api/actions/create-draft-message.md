# Create Draft Message with Outlook

Creates a draft email in Outlook.

## Endpoint

- **Method:** `POST`
- **Path:** `/me/messages`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Create Draft Message](https://learn.microsoft.com/en-us/graph/api/user-post-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `string` | yes | Draft message subject. |
| `body.content` | body | `string` | yes | Draft message body content. |
| `body.contentType` | body | `list` | yes | Message body content type: Text or HTML. Accepted values: `0`, `1`. |
| `toRecipients[]` | body | `array<object>` | no | Recipient array in Microsoft Graph format, for example [{"emailAddress":{"address":"person@example.com"}}]. |
