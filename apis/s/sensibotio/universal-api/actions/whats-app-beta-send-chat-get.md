# Sensibot.io: WhatsApp beta Send Chat [GET]

Sends a WhatsApp beta chat message through Sensibot.io using GET.

```
POST https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/whats-app-beta-send-chat-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sensibot.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/whats-app-beta-send-chat-get" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/whats-app-beta-send-chat-get', {
  method: 'POST',
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
| `isGroup` | string | no |  |
| `message` | string | no |  |
| `recipient` | string | no |  |
| `token` | string | no |  |
| `type` | string | no |  |
| `waNumber` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        [
          {}
        ]
      ],
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
| `data[]` | array<object> |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Sensibot.io API, this operation is `GET /whatsappbeta/send_get` (base URL `https://api.sensibot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/whats-app-beta-send-chat-get.md) for the provider-specific parameters and requirements.

