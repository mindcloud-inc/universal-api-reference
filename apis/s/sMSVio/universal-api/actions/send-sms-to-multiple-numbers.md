# SMSVio: Send SMS to Multiple Numbers



```
POST https://connect.mindcloud.co/v1/universal/sMSVio/latest/actions/send-sms-to-multiple-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSVio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSVio/latest/actions/send-sms-to-multiple-numbers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSVio/latest/actions/send-sms-to-multiple-numbers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages` | string<object> | yes | JSON string array of {number, message} objects to send |
| `useAvailable` | boolean | no | Prefer an available device for delivery |
| `devices` | string | no | Optional device identifiers to use for delivery |

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

Through the native SMSVio API, this operation is `POST /services/send/` (base URL `https://gate.smsvio.cz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms-to-multiple-numbers.md) for the provider-specific parameters and requirements.

