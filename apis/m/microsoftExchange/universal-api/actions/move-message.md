# Microsoft Exchange: Move Message

Moves a message to another folder in Microsoft Exchange.

```
PUT https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/move-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Exchange `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/move-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "AAMkAG...",
  "destinationId": "deleteditems"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/move-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "AAMkAG...",
    "destinationId": "deleteditems"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | The ID of the Exchange message to move. Example: `AAMkAG...`. |
| `destinationId` | string | yes | The destination folder ID or a well-known Exchange folder name such as deleteditems or archive. Example: `deleteditems`. |

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
| `id` | string | The moved message ID. |
| `subject` | string | The message subject line. |
| `webLink` | string | A link to open the message in Outlook on the web. |

## Native endpoint

Through the native Microsoft Exchange API, this operation is `POST /v1.0/me/messages/{{messageId}}/move` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-message.md) for the provider-specific parameters and requirements.

