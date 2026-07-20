# Microsoft 365 Outlook: Add File Attachment to Message

Adds a file attachment to a message in Microsoft 365 Outlook.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/add-file-attachment-to-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Outlook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/add-file-attachment-to-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "string",
  "name": "Ava Chen",
  "contentType": "text/plain",
  "contentBytes": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/add-file-attachment-to-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "string",
    "name": "Ava Chen",
    "contentType": "text/plain",
    "contentBytes": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | The draft or message ID to attach the file to. |
| `name` | string | yes | Name of the file attachment. |
| `contentType` | string | yes | MIME type of the attachment content. Default: `text/plain`. |
| `contentBytes` | string | yes | Base64-encoded file content. Microsoft Graph supports this action for attachments under 3 MB. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@odata": {
        "type": "string"
      },
      "contentBytes": "string",
      "contentType": "string",
      "id": "string",
      "isInline": true,
      "lastModifiedDateTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@odata.type` | string | Microsoft Graph attachment resource discriminator. |
| `contentBytes` | string | Base64-encoded attachment content returned by Microsoft Graph. |
| `contentType` | string | Attachment MIME type. |
| `id` | string | Microsoft Graph attachment ID. |
| `isInline` | boolean | Whether the attachment is inline. |
| `lastModifiedDateTime` | date | When the attachment was last modified. |
| `name` | string | Attachment file name. |
| `size` | number | Attachment size in bytes. |

## Native endpoint

Through the native Microsoft 365 Outlook API, this operation is `POST /v1.0/me/messages/{{messageId}}/attachments` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-file-attachment-to-message.md) for the provider-specific parameters and requirements.

