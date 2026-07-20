# SMSVio: Send SMS



```
POST https://connect.mindcloud.co/v1/universal/sMSVio/latest/actions/send-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSVio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSVio/latest/actions/send-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string",
  "number": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSVio/latest/actions/send-sms', {
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
| `message` | string | yes | SMS body text to send |
| `number` | string | yes | Recipient phone number in international format |
| `devices` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "error": {},
      "status": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `error` | object |  |
| `status` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native SMSVio API, this operation is `POST /services/send/` (base URL `https://gate.smsvio.cz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms.md) for the provider-specific parameters and requirements.

