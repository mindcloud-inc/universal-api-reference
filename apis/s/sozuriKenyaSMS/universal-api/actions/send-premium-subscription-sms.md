# Sozuri (Kenya) SMS: Send Premium Subscription SMS

Sends a subscription premium SMS through Sozuri.

```
POST https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/send-premium-subscription-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sozuri (Kenya) SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/send-premium-subscription-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "to": "string",
  "message": "string",
  "linkId": "https://example.com",
  "keyword": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/send-premium-subscription-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "to": "string",
    "message": "string",
    "linkId": "https://example.com",
    "keyword": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | The premium shortcode sender defined in your project. |
| `to` | string | yes | A recipient phone number in E.164 format. |
| `campaign` | string | no | The campaign name for this message. |
| `message` | string | yes | The premium SMS content to send. |
| `linkId` | string | yes | The link ID for this premium request. |
| `keyword` | string | yes | The premium service keyword. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messageData": {},
      "recipients": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messageData` | object |  |
| `recipients` | array<object> |  |

## Native endpoint

Through the native Sozuri (Kenya) SMS API, this operation is `POST /premium` (base URL `https://sozuri.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-premium-subscription-sms.md) for the provider-specific parameters and requirements.

