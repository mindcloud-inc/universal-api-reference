# Outlook: Update Message

Updates an existing Outlook email, with some fields draft-only.

```
PUT https://connect.mindcloud.co/v1/universal/outlook/latest/actions/update-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/outlook/latest/actions/update-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outlook/latest/actions/update-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | Microsoft Graph ID of the message to update. |
| `subject` | string | no | New message subject. Updatable only for drafts. Example: `Updated subject`. |
| `bodyContent` | string | no | New message body content. Updatable only for drafts. Example: `Updated message body.`. |
| `bodyContentType` | list | no | Message body content type: Text or HTML. One of: `0`, `1`. Default: `Text`. |
| `isRead` | boolean | no | Whether the message should be marked as read. |
| `categories[]` | array<string> | no | Categories to apply to the message. |
| `importance` | list | no | Message importance: low, normal, or high. One of: `0`, `1`, `2`. |
| `inferenceClassification` | list | no | Focused inbox classification: focused or other. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bccRecipients": [
        {
          "emailAddress": {
            "address": "ava@example.com",
            "name": "ava@example.com"
          }
        }
      ],
      "body": {
        "content": "string",
        "contentType": "string"
      },
      "bodyPreview": "string",
      "categories": [
        "string"
      ],
      "ccRecipients": [
        {
          "emailAddress": {
            "address": "ava@example.com",
            "name": "ava@example.com"
          }
        }
      ],
      "changeKey": "string",
      "conversationId": "string",
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "flag": {
        "flagStatus": "string"
      },
      "hasAttachments": true,
      "id": "string",
      "importance": "string",
      "internetMessageId": "string",
      "isDraft": true,
      "isRead": true,
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "parentFolderId": "string",
      "receivedDateTime": "2026-05-07T12:00:00.000Z",
      "sentDateTime": "2026-05-07T12:00:00.000Z",
      "subject": "string",
      "toRecipients": [
        {
          "emailAddress": {
            "address": "ava@example.com",
            "name": "ava@example.com"
          }
        }
      ],
      "webLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bccRecipients[].emailAddress.address` | string | BCC recipient email address. |
| `bccRecipients[].emailAddress.name` | string | BCC recipient display name. |
| `body.content` | string | Full message body content. |
| `body.contentType` | string | Message body content type. |
| `bodyPreview` | string | First 255 characters of the message body. |
| `categories` | array<string> | Categories assigned to the message. |
| `ccRecipients[].emailAddress.address` | string | CC recipient email address. |
| `ccRecipients[].emailAddress.name` | string | CC recipient display name. |
| `changeKey` | string | Version identifier for the message. |
| `conversationId` | string | ID of the conversation the message belongs to. |
| `createdDateTime` | date | Date and time when the message was created. |
| `flag.flagStatus` | string | Follow-up flag status. |
| `hasAttachments` | boolean | Whether the message has attachments. |
| `id` | string | Microsoft Graph message ID. |
| `importance` | string | Message importance. |
| `internetMessageId` | string | RFC 2822 internet message ID. |
| `isDraft` | boolean | Whether the message is a draft. |
| `isRead` | boolean | Whether the message has been read. |
| `lastModifiedDateTime` | date | Date and time when the message was last modified. |
| `parentFolderId` | string | ID of the folder containing the message. |
| `receivedDateTime` | date | Date and time when the message was received. |
| `sentDateTime` | date | Date and time when the message was sent. |
| `subject` | string | Message subject. |
| `toRecipients[].emailAddress.address` | string | Recipient email address. |
| `toRecipients[].emailAddress.name` | string | Recipient display name. |
| `webLink` | string | Outlook on the web URL for the message. |

## Native endpoint

Through the native Outlook API, this operation is `PATCH /me/messages/:messageId` (base URL `https://graph.microsoft.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-message.md) for the provider-specific parameters and requirements.

