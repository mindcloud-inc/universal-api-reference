# Outlook: Create Draft Message

Creates a draft email in Outlook.

```
POST https://connect.mindcloud.co/v1/universal/outlook/latest/actions/create-draft-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/outlook/latest/actions/create-draft-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "Quarterly update",
  "bodyContent": "Write the draft body here.",
  "bodyContentType": "Text"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outlook/latest/actions/create-draft-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "Quarterly update",
    "bodyContent": "Write the draft body here.",
    "bodyContentType": "Text"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | yes | Draft message subject. Example: `Quarterly update`. |
| `bodyContent` | string | yes | Draft message body content. Example: `Write the draft body here.`. |
| `bodyContentType` | list | yes | Message body content type: Text or HTML. One of: `0`, `1`. Default: `Text`. |
| `toRecipients[]` | array<object> | no | Recipient array in Microsoft Graph format, for example [{"emailAddress":{"address":"person@example.com"}}]. |

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

Through the native Outlook API, this operation is `POST /me/messages` (base URL `https://graph.microsoft.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-draft-message.md) for the provider-specific parameters and requirements.

