# Microsoft Exchange: List User Messages in Mailbox

Finds messages in a user's mailbox.

```
GET https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/list-user-messages-in-mailbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Exchange `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/list-user-messages-in-mailbox?connectionId=$CONNECTION_ID&limit=25&offset=0&userIdOrPrincipalName=user%40company.com%20or%20Entra%20user%20id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userIdOrPrincipalName": "user@company.com or Entra user id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/list-user-messages-in-mailbox?${params}`, {
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
| `top` | number | no | Maximum number of messages to return. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderBy` | string | no | Optional Microsoft Graph $orderby expression. Use sentDateTime desc for sentitems and receivedDateTime desc for inbox. Default: `receivedDateTime desc`. Example: `receivedDateTime desc`. |
| `select` | string | no | Comma-separated Microsoft Graph message fields to return. Default: `id,subject,receivedDateTime,sentDateTime,bodyPreview,hasAttachments,importance,isRead,from,sender,toRecipients,ccRecipients,bccRecipients,webLink`. |
| `expand` | string | no | Optional Microsoft Graph $expand expression. The default returns attachment metadata including isInline so inline images can be counted. Default: `attachments($select=id,name,contentType,isInline)`. Example: `attachments($select=id,name,contentType,isInline)`. |
| `filter` | string | no | Optional Microsoft Graph OData filter expression. |
| `$count` | string | no | Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@odata": {
        "etag": "string"
      },
      "from": {
        "emailAddress": {
          "address": "ava@example.com",
          "name": "ava@example.com"
        }
      },
      "hasAttachments": true,
      "id": "string",
      "parentFolderId": "string",
      "receivedDateTime": "string",
      "sender": {
        "emailAddress": {
          "address": "ava@example.com",
          "name": "ava@example.com"
        }
      },
      "sentDateTime": "string",
      "toRecipients": [
        {
          "emailAddress": {
            "address": "ava@example.com",
            "name": "ava@example.com"
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@odata.etag` | string |  |
| `from.emailAddress.address` | string |  |
| `from.emailAddress.name` | string |  |
| `hasAttachments` | boolean |  |
| `id` | string |  |
| `parentFolderId` | string |  |
| `receivedDateTime` | string |  |
| `sender.emailAddress.address` | string |  |
| `sender.emailAddress.name` | string |  |
| `sentDateTime` | string |  |
| `toRecipients[].emailAddress.address` | string |  |
| `toRecipients[].emailAddress.name` | string |  |

## Native endpoint

Through the native Microsoft Exchange API, this operation is `GET /v1.0/users/:userIdOrPrincipalName/messages` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-messages-in-mailbox.md) for the provider-specific parameters and requirements.

