# Microsoft 365 Outlook: List Message Attachments

Retrieves attachments for a message from Microsoft 365 Outlook.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/list-message-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Outlook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/list-message-attachments?connectionId=$CONNECTION_ID&messageId=AAMkAG..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "AAMkAG..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/list-message-attachments?${params}`, {
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
| `messageId` | string | yes | The Outlook message ID whose attachments you want to list. Example: `AAMkAG...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `contentType` | string | The attachment MIME type. |
| `id` | string | The attachment ID. |
| `isInline` | boolean | Whether the attachment is inline. |
| `lastModifiedDateTime` | date | When the attachment was last modified. |
| `name` | string | The attachment file name. |
| `size` | number | The attachment size in bytes. |

## Native endpoint

Through the native Microsoft 365 Outlook API, this operation is `GET /v1.0/me/messages/{{messageId}}/attachments` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-message-attachments.md) for the provider-specific parameters and requirements.

