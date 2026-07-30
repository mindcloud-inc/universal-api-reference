# Microsoft Exchange: List User Messages in Folder

Finds messages in a user's mail folder in Microsoft Exchange.

```
GET https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/list-user-messages-in-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Exchange `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/list-user-messages-in-folder?connectionId=$CONNECTION_ID&userIdOrPrincipalName=user%40company.com%20or%20Entra%20user%20id&mailFolderId=sentitems" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userIdOrPrincipalName": "user@company.com or Entra user id",
  "mailFolderId": "sentitems"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/list-user-messages-in-folder?${params}`, {
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
| `userIdOrPrincipalName` | string | yes | The Microsoft Graph user id or userPrincipalName for the mailbox whose folder messages should be listed. Use the Entra user id when the mail address differs from the userPrincipalName. Example: `user@company.com or Entra user id`. |
| `mailFolderId` | string | yes | The Microsoft Graph mail folder ID or lowercase well-known folder name, such as inbox or sentitems. If a well-known name is not found for a mailbox, list that user's folders and pass the returned folder id. Default: `inbox`. Example: `sentitems`. |
| `top` | number | no | Maximum number of messages to return. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderBy` | string | no | Optional Microsoft Graph $orderby expression. Use sentDateTime desc for sentitems and receivedDateTime desc for inbox. Default: `receivedDateTime desc`. Example: `receivedDateTime desc`. |
| `select` | string | no | Comma-separated Microsoft Graph message fields to return. Default: `id,subject,receivedDateTime,sentDateTime,bodyPreview,hasAttachments,importance,isRead,from,sender,toRecipients,ccRecipients,bccRecipients,webLink`. |
| `expand` | string | no | Optional Microsoft Graph $expand expression. The default returns attachment metadata including isInline so inline images can be counted. Default: `attachments($select=id,name,contentType,isInline)`. Example: `attachments($select=id,name,contentType,isInline)`. |
| `filter` | string | no | Optional Microsoft Graph OData filter expression. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {
          "contentType": "string",
          "id": "string",
          "isInline": true,
          "name": "Ava Chen"
        }
      ],
      "bccRecipients": [
        {
          "emailAddress": {
            "address": "ava@example.com",
            "name": "ava@example.com"
          }
        }
      ],
      "bodyPreview": "string",
      "ccRecipients": [
        {
          "emailAddress": {
            "address": "ava@example.com",
            "name": "ava@example.com"
          }
        }
      ],
      "from": {
        "emailAddress": {
          "address": "ava@example.com",
          "name": "ava@example.com"
        }
      },
      "hasAttachments": true,
      "id": "string",
      "importance": "string",
      "isRead": true,
      "receivedDateTime": "2026-05-07T12:00:00.000Z",
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
| `attachments[].contentType` | string | The attachment content type. |
| `attachments[].id` | string | The attachment ID. |
| `attachments[].isInline` | boolean | Whether the attachment is inline content, such as an embedded image. |
| `attachments[].name` | string | The attachment file name or inline content name. |
| `bccRecipients[].emailAddress.address` | string | The email address of a Bcc recipient. |
| `bccRecipients[].emailAddress.name` | string | The display name of a Bcc recipient. |
| `bodyPreview` | string | A text preview of the message body. |
| `ccRecipients[].emailAddress.address` | string | The email address of a Cc recipient. |
| `ccRecipients[].emailAddress.name` | string | The display name of a Cc recipient. |
| `from.emailAddress.address` | string | The sender email address. |
| `from.emailAddress.name` | string | The display name of the sender. |
| `hasAttachments` | boolean | Whether the message has non-inline attachments according to Microsoft Graph. Inline-only attachments can still appear in attachments[]. |
| `id` | string | The Microsoft Graph message ID. |
| `importance` | string | The message importance level. |
| `isRead` | boolean | Whether the message has been read. |
| `receivedDateTime` | date | When the message was received. |
| `sender.emailAddress.address` | string | The sending account email address. |
| `sender.emailAddress.name` | string | The display name of the sending account. |
| `sentDateTime` | date | When the message was sent. |
| `subject` | string | The message subject line. |
| `toRecipients[].emailAddress.address` | string | The email address of a To recipient. |
| `toRecipients[].emailAddress.name` | string | The display name of a To recipient. |
| `webLink` | string | A link to open the message in Outlook on the web. |

## Native endpoint

Through the native Microsoft Exchange API, this operation is `GET /v1.0/users/:userIdOrPrincipalName/mailFolders/:mailFolderId/messages` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-messages-in-folder.md) for the provider-specific parameters and requirements.

