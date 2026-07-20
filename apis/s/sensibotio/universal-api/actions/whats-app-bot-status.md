# Sensibot.io: WhatsApp Bot Status

Updates the WhatsApp beta bot status in Sensibot.io.

```
PUT https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/whats-app-bot-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sensibot.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/whats-app-bot-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/whats-app-bot-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botStatus` | string | no |  |
| `waNumber` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Sensibot.io API, this operation is `POST /whatsappbeta/bot_status` (base URL `https://api.sensibot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/whats-app-bot-status.md) for the provider-specific parameters and requirements.

