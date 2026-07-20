# TopMessage: Send SMS Template Message

Creates an SMS template message in TopMessage.

```
POST https://connect.mindcloud.co/v1/universal/topMessage/latest/actions/send-sms-template-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TopMessage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/topMessage/latest/actions/send-sms-template-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "to[]": [
    "string"
  ],
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/topMessage/latest/actions/send-sms-template-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "to[]": ["string"],
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | The sender name or virtual number the message appears to come from. |
| `to[]` | array<string> | yes | One or more recipient phone numbers in international format. |
| `templateId` | string | yes | The existing TopMessage template identifier to send. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | The template-based message returned by TopMessage. |

## Native endpoint

Through the native TopMessage API, this operation is `POST /v1/messages` (base URL `https://api.topmessage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms-template-message.md) for the provider-specific parameters and requirements.

