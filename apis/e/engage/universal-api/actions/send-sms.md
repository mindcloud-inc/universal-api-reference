# Engage: Send SMS

Sends a transactional SMS through Engage.

```
POST https://connect.mindcloud.co/v1/universal/engage/latest/actions/send-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Engage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/engage/latest/actions/send-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "source": "string",
  "to": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/engage/latest/actions/send-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "source": "string",
    "to": "string",
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channel` | string | no | Optional SMS channel, such as generic or dnd for supported providers. |
| `from` | string | yes | Sender ID registered with your SMS provider. |
| `trackClicks` | boolean | no | Set to true to enable click tracking. |
| `source` | string | yes | SMS integration to send with, such as twilio or termii. |
| `to` | string | yes | Recipient phone number with country code. |
| `body` | string | yes | Message body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Identifier of the sent transactional SMS message. |

## Native endpoint

Through the native Engage API, this operation is `POST /send/sms` (base URL `https://api.engage.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms.md) for the provider-specific parameters and requirements.

