# Pushpad: Update Sender

Updates an existing sender in Pushpad.

```
PUT https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/update-sender
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/update-sender" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "senderId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/update-sender', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "senderId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no |  |
| `senderId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": 1,
      "name": "Ava Chen",
      "vapidPrivateKey": "string",
      "vapidPublicKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | number |  |
| `name` | string |  |
| `vapidPrivateKey` | string |  |
| `vapidPublicKey` | string |  |

## Native endpoint

Through the native Pushpad API, this operation is `PATCH /senders/:sender_id` (base URL `https://pushpad.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sender.md) for the provider-specific parameters and requirements.

