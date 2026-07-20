# Salebot: Send Broadcast



```
POST https://connect.mindcloud.co/v1/universal/salebot/latest/actions/send-broadcast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salebot/latest/actions/send-broadcast" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salebot/latest/actions/send-broadcast', {
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
| `clients[]` | array<number> | no | Target Salebot client IDs. |
| `platformIds[]` | array<string> | no | Target platform IDs when sending via a specific connected channel. |
| `groupId` | number | no | Connected channel group ID used with platform_ids. |
| `listId` | number | no | Salebot list identifier to broadcast to. |
| `messageId` | number | no | Bot block ID to broadcast instead of raw text. |
| `message` | string | no | Broadcast message text. |

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
| `response` | string |  |

## Native endpoint

Through the native Salebot API, this operation is `POST /broadcast` (base URL `https://chatter.salebot.pro/api/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-broadcast.md) for the provider-specific parameters and requirements.

