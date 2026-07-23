# Microsoft Exchange: Get Message Attachment

Retrieves a message attachment from Microsoft Exchange.

```
GET https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/get-message-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Exchange `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/get-message-attachment?connectionId=$CONNECTION_ID&messageId=AAMkAG...&attachmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "AAMkAG...",
  "attachmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/get-message-attachment?${params}`, {
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
| `messageId` | string | yes | The Exchange message ID that contains the attachment. Example: `AAMkAG...`. |
| `attachmentId` | string | yes | The Exchange attachment ID returned by the attachment list action. |

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

Through the native Microsoft Exchange API, this operation is `GET /v1.0/me/messages/{{messageId}}/attachments/{{attachmentId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-attachment.md) for the provider-specific parameters and requirements.

