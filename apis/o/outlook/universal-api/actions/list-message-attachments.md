# Outlook: List Message Attachments

Retrieves attachments for an Outlook email.

```
GET https://connect.mindcloud.co/v1/universal/outlook/latest/actions/list-message-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outlook/latest/actions/list-message-attachments?connectionId=$CONNECTION_ID&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outlook/latest/actions/list-message-attachments?${params}`, {
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
| `messageId` | string | yes | Microsoft Graph ID of the Outlook message whose attachments should be listed. |

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
      "contentId": "string",
      "contentLocation": "string",
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
| `@odata.type` | string | Microsoft Graph attachment derived type. |
| `contentBytes` | string | Base64-encoded file contents for file attachments when returned by Graph. |
| `contentId` | string | Content ID for inline file attachments. |
| `contentLocation` | string | Content location for the attachment when provided. |
| `contentType` | string | Attachment MIME content type. |
| `id` | string | Microsoft Graph attachment ID. |
| `isInline` | boolean | Whether the attachment is inline. |
| `lastModifiedDateTime` | date | Date and time when the attachment was last modified. |
| `name` | string | Attachment file or item name. |
| `size` | number | Attachment size in bytes. |

## Native endpoint

Through the native Outlook API, this operation is `GET /me/messages/:messageId/attachments` (base URL `https://graph.microsoft.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-message-attachments.md) for the provider-specific parameters and requirements.

