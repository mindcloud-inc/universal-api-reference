# Microsoft 365 Outlook: List Messages in Folder

Retrieves messages from a mail folder in Microsoft 365 Outlook.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/list-messages-in-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Outlook `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/list-messages-in-folder?connectionId=$CONNECTION_ID&limit=25&offset=0&mailFolderId=inbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "mailFolderId": "inbox"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/list-messages-in-folder?${params}`, {
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
| `mailFolderId` | string | yes | The mail folder ID or a well-known folder name such as inbox or archive. Example: `inbox`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bodyPreview": "string",
      "categories": [
        "string"
      ],
      "from": {
        "emailAddress": {
          "address": "ava@example.com"
        }
      },
      "hasAttachments": true,
      "id": "string",
      "isRead": true,
      "receivedDateTime": "2026-05-07T12:00:00.000Z",
      "sentDateTime": "2026-05-07T12:00:00.000Z",
      "subject": "string",
      "webLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bodyPreview` | string | A text preview of the message body. |
| `categories` | array<string> | The categories (tags) assigned to the message. |
| `from.emailAddress.address` | string | The sender email address. |
| `hasAttachments` | boolean | Whether the message has attachments. |
| `id` | string | The Microsoft Graph message ID. |
| `isRead` | boolean | Whether the message has been read. |
| `receivedDateTime` | date | When the message was received. |
| `sentDateTime` | date | When the message was sent. |
| `subject` | string | The message subject line. |
| `webLink` | string | A link to open the message in Outlook on the web. |

## Native endpoint

Through the native Microsoft 365 Outlook API, this operation is `GET /v1.0/me/mailFolders/{{mailFolderId}}/messages` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messages-in-folder.md) for the provider-specific parameters and requirements.

