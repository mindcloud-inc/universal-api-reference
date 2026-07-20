# Microsoft 365: Get Message Attachment

Retrieves a message attachment from Microsoft 365.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/get-message-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/get-message-attachment?connectionId=$CONNECTION_ID&messageId=string&attachmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string",
  "attachmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/get-message-attachment?${params}`, {
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
| `messageId` | string | yes | The Outlook message ID that contains the attachment. |
| `attachmentId` | string | yes | The Outlook attachment ID returned by the attachment list action. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentBytes": "string",
      "contentId": "string",
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
| `contentBytes` | string | Base64-encoded file contents for file attachments. |
| `contentId` | string |  |
| `contentType` | string |  |
| `id` | string |  |
| `isInline` | boolean |  |
| `lastModifiedDateTime` | date |  |
| `name` | string |  |
| `size` | number |  |

## Native endpoint

Through the native Microsoft 365 API, this operation is `GET /v1.0/me/messages/{{messageId}}/attachments/{{attachmentId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-attachment.md) for the provider-specific parameters and requirements.

