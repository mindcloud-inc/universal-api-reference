# Microsoft 365: Get Message

Retrieves a message from Microsoft 365.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/get-message?connectionId=$CONNECTION_ID&messageId=AAMkAG..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "AAMkAG..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/get-message?${params}`, {
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
      "internetMessageId": "string",
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
| `bodyPreview` | string |  |
| `hasAttachments` | boolean |  |
| `id` | string |  |
| `importance` | string |  |
| `internetMessageId` | string |  |
| `isDraft` | boolean |  |
| `isRead` | boolean |  |
| `receivedDateTime` | date |  |
| `sentDateTime` | date |  |
| `subject` | string |  |
| `webLink` | string |  |

## Native endpoint

Through the native Microsoft 365 API, this operation is `GET /v1.0/me/messages/{{messageId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

