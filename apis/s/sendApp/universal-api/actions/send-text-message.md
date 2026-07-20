# SendApp: Send Text Message



```
POST https://connect.mindcloud.co/v1/universal/sendApp/latest/actions/send-text-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendApp/latest/actions/send-text-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string",
  "number": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendApp/latest/actions/send-text-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string",
    "number": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `footer` | string | no | Optional footer text. |
| `header` | string | no | Optional header text. |
| `message` | string | yes | Text message to send. |
| `number` | string | yes | WhatsApp number in international format with the + prefix. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Provider docs do not publish a structured send-text success response example. |

## Native endpoint

Through the native SendApp API, this operation is `GET /send/text` (base URL `https://official.sendapp.cloud/apiv3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-text-message.md) for the provider-specific parameters and requirements.

