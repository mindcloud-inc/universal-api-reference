# Microsoft 365: Update Draft Message

Updates a draft message in Microsoft 365.

```
PUT https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/update-draft-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/update-draft-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "AAMkAG..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/update-draft-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "AAMkAG..."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | The ID of the Outlook message to update. Example: `AAMkAG...`. |
| `subject` | string | no | Updated message subject. This is most useful when editing a draft message. Example: `Updated draft subject`. |
| `body.content` | string | no | Updated message body content. This is most useful when editing a draft message. Example: `Updated message body content`. |

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
      "receivedDateTime": "string",
      "sentDateTime": "string",
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
| `receivedDateTime` | string |  |
| `sentDateTime` | string |  |
| `subject` | string |  |
| `webLink` | string |  |

## Native endpoint

Through the native Microsoft 365 API, this operation is `PATCH /v1.0/me/messages/{{messageId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-draft-message.md) for the provider-specific parameters and requirements.

