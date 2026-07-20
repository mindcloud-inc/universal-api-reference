# Microsoft 365 Outlook: Update Draft Message

Updates an existing draft message in Microsoft 365 Outlook.

```
PUT https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/update-draft-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Outlook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/update-draft-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "AAMkAG..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Outlook/latest/actions/update-draft-message', {
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
      "id": "string",
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
| `id` | string | The updated message ID. |
| `subject` | string | The message subject line. |
| `webLink` | string | A link to open the message in Outlook on the web. |

## Native endpoint

Through the native Microsoft 365 Outlook API, this operation is `PATCH /v1.0/me/messages/{{messageId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-draft-message.md) for the provider-specific parameters and requirements.

