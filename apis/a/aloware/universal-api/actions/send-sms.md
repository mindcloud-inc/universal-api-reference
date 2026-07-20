# Aloware: Send SMS

Sends an SMS or MMS message from Aloware.

```
POST https://connect.mindcloud.co/v1/universal/aloware/latest/actions/send-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aloware `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aloware/latest/actions/send-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aloware/latest/actions/send-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | no | Sender phone number. Provide this or Line ID. |
| `lineId` | string | no | Aloware line ID to send from. Provide this or From Number. |
| `to` | string | yes | Recipient phone number. |
| `message` | string | yes | SMS or MMS message content. |
| `imageUrl` | string | no | Optional image URL to send as MMS. |
| `forceRandom` | string | no | Set to 1 to ignore number stickiness and distribute randomly. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aloware API returns.

## Native endpoint

Through the native Aloware API, this operation is `POST /api/v1/webhook/sms-gateway/send` (base URL `https://app.aloware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms.md) for the provider-specific parameters and requirements.

