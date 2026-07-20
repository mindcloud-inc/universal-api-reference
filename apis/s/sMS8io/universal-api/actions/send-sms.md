# SMS8.io: Send SMS



```
POST https://connect.mindcloud.co/v1/universal/sMS8io/latest/actions/send-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS8.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMS8io/latest/actions/send-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "number": "string",
  "message": "string",
  "devices": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMS8io/latest/actions/send-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "number": "string",
    "message": "string",
    "devices": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `number` | string | yes | Recipient phone number. |
| `message` | string | yes | SMS body text (URL-encoded by the platform). |
| `devices` | string | yes | JSON-encoded array of devices and SIM slots, for example ["182\|0","182\|1"]. |
| `prioritize` | number | no | Prioritize device for sending when multiple devices are available. Default: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SMS8.io API returns.

## Native endpoint

Through the native SMS8.io API, this operation is `GET send.php` (base URL `https://app.sms8.io/services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms.md) for the provider-specific parameters and requirements.

