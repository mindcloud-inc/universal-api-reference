# Outlook: Get Message

Retrieves an email from Outlook by message ID.

```
GET https://connect.mindcloud.co/v1/universal/outlook/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outlook/latest/actions/get-message?connectionId=$CONNECTION_ID&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outlook/latest/actions/get-message?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | Microsoft Graph ID of the Outlook message to retrieve. |

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
      "conversationIndex": "string",
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "flag": {
        "flagStatus": "string"
      },
      "from": {
        "emailAddress": {
          "address": "ava@example.com",
          "name": "ava@example.com"
        }
      },
      "hasAttachments": true,
      "id": "string",
      "importance": "string",
      "inferenceClassification": "string",
      "internetMessageId": "string",
      "isDeliveryReceiptRequested": true,
      "isDraft": true,
      "isRead": true,
      "isReadReceiptRequested": true,
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "parentFolderId": "string",
      "receivedDateTime": "2026-05-07T12:00:00.000Z",
      "replyTo": [
        {
          "emailAddress": {
            "address": "ava@example.com",
            "name": "ava@example.com"
          }
        }
      ],
      "sender": {
        "emailAddress": {
          "address": "ava@example.com",
          "name": "ava@example.com"
        }
      },
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
| `conversationIndex` | string | Conversation index value. |
| `createdDateTime` | date | Date and time when the message was created. |
| `flag.flagStatus` | string | Follow-up flag status. |
| `from.emailAddress.address` | string | From email address. |
| `from.emailAddress.name` | string | From display name. |
| `hasAttachments` | boolean | Whether the message has attachments. |
| `id` | string | Microsoft Graph message ID. |
| `importance` | string | Message importance. |
| `inferenceClassification` | string | Focused or other inbox classification. |
| `internetMessageId` | string | RFC 2822 internet message ID. |
| `isDeliveryReceiptRequested` | boolean | Whether delivery receipt was requested. |
| `isDraft` | boolean | Whether the message is a draft. |
| `isRead` | boolean | Whether the message has been read. |
| `isReadReceiptRequested` | boolean | Whether read receipt was requested. |
| `lastModifiedDateTime` | date | Date and time when the message was last modified. |
| `parentFolderId` | string | ID of the folder containing the message. |
| `receivedDateTime` | date | Date and time when the message was received. |
| `replyTo[].emailAddress.address` | string | Reply-to email address. |
| `replyTo[].emailAddress.name` | string | Reply-to display name. |
| `sender.emailAddress.address` | string | Sender email address. |
| `sender.emailAddress.name` | string | Sender display name. |
| `sentDateTime` | date | Date and time when the message was sent. |
| `subject` | string | Message subject. |
| `toRecipients[].emailAddress.address` | string | Recipient email address. |
| `toRecipients[].emailAddress.name` | string | Recipient display name. |
| `webLink` | string | Outlook on the web URL for the message. |

## Native endpoint

Through the native Outlook API, this operation is `GET /me/messages/:messageId` (base URL `https://graph.microsoft.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

