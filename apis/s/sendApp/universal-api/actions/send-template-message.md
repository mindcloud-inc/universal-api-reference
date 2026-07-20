# SendApp: Send Template Message



```
POST https://connect.mindcloud.co/v1/universal/sendApp/latest/actions/send-template-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendApp/latest/actions/send-template-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "languageCode": "string",
  "number": "string",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendApp/latest/actions/send-template-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "languageCode": "string",
    "number": "string",
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `button1` | string | no | Optional first button payload. |
| `button2` | string | no | Optional second button payload. |
| `button3` | string | no | Optional third button payload. |
| `headerMedia` | string | no | Optional header image or video URL. |
| `languageCode` | string | yes | Template language code such as en, it, or es. |
| `number` | string | yes | WhatsApp number in international format with the + prefix. |
| `param1` | string | no | Optional first template parameter. |
| `param2` | string | no | Optional second template parameter. |
| `param3` | string | no | Optional third template parameter. |
| `templateId` | string | yes | Approved template ID. |

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
| `response` | string | Provider docs do not publish a structured send-template success response example. |

## Native endpoint

Through the native SendApp API, this operation is `GET /send/template` (base URL `https://official.sendapp.cloud/apiv3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-template-message.md) for the provider-specific parameters and requirements.

