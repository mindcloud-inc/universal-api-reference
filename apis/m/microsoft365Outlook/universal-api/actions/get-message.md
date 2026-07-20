# Microsoft 365 Outlook: Get Message

Retrieves a message from Microsoft 365 Outlook.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Outlook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/get-message?connectionId=$CONNECTION_ID&messageId=AAMkAG..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "AAMkAG..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/get-message?${params}`, {
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
| `messageId` | string | yes | The ID of the Outlook message. Example: `AAMkAG...`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bodyPreview": "string",
      "hasAttachments": true,
      "id": "string",
      "importance": "string",
      "isDraft": true,
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
| `hasAttachments` | boolean | Whether the message has attachments. |
| `id` | string | The Microsoft Graph message ID. |
| `importance` | string | The message importance level. |
| `isDraft` | boolean | Whether the message is a draft. |
| `isRead` | boolean | Whether the message has been read. |
| `receivedDateTime` | date | When the message was received. |
| `sentDateTime` | date | When the message was sent. |
| `subject` | string | The message subject line. |
| `webLink` | string | A link to open the message in Outlook on the web. |

## Native endpoint

Through the native Microsoft 365 Outlook API, this operation is `GET /v1.0/me/messages/{{messageId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

